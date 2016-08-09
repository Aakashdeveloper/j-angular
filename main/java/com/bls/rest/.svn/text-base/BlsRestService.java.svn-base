package com.bls.rest;

import java.util.ArrayList;

import javax.ws.rs.GET;
import javax.ws.rs.Path;
import javax.ws.rs.PathParam;
import javax.ws.rs.Produces;
import javax.ws.rs.core.MediaType;
import com.bls.dao.entity.place.PlacePojo;
import com.bls.services.PlaceServices;
import com.bls.services.UserServices;


@Path("/city")
public class BlsRestService {
    @GET    
    @Produces(MediaType.APPLICATION_JSON)
    @Path("/getUser")
    public com.bls.services.UserServices.User getDefaultUserInJSON() {
        UserServices userService = new UserServices();
        return userService.getDefaultUser();
    }

    
	@GET
	@Path("/getCities/{userInput}")
    @Produces(MediaType.APPLICATION_JSON)
	public ArrayList<PlacePojo> getCities(@PathParam(value="userInput")String userInput) {
		ArrayList<PlacePojo> output=null;
		output = PlaceServices.getListCityByName(userInput, true);
		return output;
	}
}
