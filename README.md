# Aws-serverless-api
exports.handler = async (event) => {
    const response = {
        success: true,
        message: "AWS Lambda API is working!",
        method: event.requestContext?.http?.method || "GET"
    };

    return {
        statusCode: 200,
        headers: {
            "Content-Type": "application/json"
        },
        body: JSON.stringify(response)
    };
};
