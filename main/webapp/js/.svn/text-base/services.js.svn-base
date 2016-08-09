'use strict';

/* Services */

var services = angular.module('ngbls.services', ['ngResource']);

services.factory('UserFactory', function ($resource) {
    return $resource('/bls-webapp/rest/city/getUser', {}, {
        query: {
            method: 'GET',
            params: {},
            isArray: false
        }
    })
});
