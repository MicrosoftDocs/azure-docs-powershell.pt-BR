---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 7b28a9ff44251e84656411d6322eb87eac9f4991
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941949"
---
# <span data-ttu-id="a3b0b-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a3b0b-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="a3b0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b0b-103">Obter os detalhes do esquema de API</span><span class="sxs-lookup"><span data-stu-id="a3b0b-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="a3b0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3b0b-104">SYNTAX</span></span>

### <span data-ttu-id="a3b0b-105">ContextParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a3b0b-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3b0b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b0b-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3b0b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3b0b-107">DESCRIPTION</span></span>
<span data-ttu-id="a3b0b-108">O cmdlet **Get-AzApiManagementApiSchema** Obtém os detalhes do esquema de API</span><span class="sxs-lookup"><span data-stu-id="a3b0b-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="a3b0b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3b0b-109">EXAMPLES</span></span>

### <span data-ttu-id="a3b0b-110">Exemplo 1: obter os detalhes de todo o esquema de API de uma API</span><span class="sxs-lookup"><span data-stu-id="a3b0b-110">Example 1 : Get the details of all the Api Schema of an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId wsdlapitest

SchemaId           : 2a03e1b4-1826-4e59-b372-4711f575db28
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <s:schema elementFormDefault="qualified"....

SchemaId           : b6e5497d-f65a-4851-9f5b-b5684cdae688
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <?xml version=""1.0"" encoding=""UTF-8""....
```

<span data-ttu-id="a3b0b-111">Esse comando obtém todos os esquemas de API associados a uma API `swagger-petstore-extensive` para um contexto ApiManagement específico.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="a3b0b-112">Exemplo 2: obter o esquema específico associado a uma API</span><span class="sxs-lookup"><span data-stu-id="a3b0b-112">Example 2 : Get the specific schema associated with an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaId 5cc9cf67e6ed3b1154e638bd

SchemaId           : 5cc9cf67e6ed3b1154e638bd
Api Id             : swagger-petstore-extensive
Schema ContentType : swaggerdefinition
Schema Document    : {
                       "definitions": {
                         "pet": {
                        ....
```

<span data-ttu-id="a3b0b-113">Esse comando obtém o esquema de API `5cc9cf67e6ed3b1154e638bd` associado a uma API `swagger-petstore-extensive` para determinado contexto ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="a3b0b-114">OS</span><span class="sxs-lookup"><span data-stu-id="a3b0b-114">PARAMETERS</span></span>

### <span data-ttu-id="a3b0b-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a3b0b-115">-ApiId</span></span>
<span data-ttu-id="a3b0b-116">Identificador de API a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-116">API identifier to look for.</span></span>
<span data-ttu-id="a3b0b-117">Se especificado, você tentará obter a API pela ID.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b0b-118">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a3b0b-118">-Context</span></span>
<span data-ttu-id="a3b0b-119">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a3b0b-120">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3b0b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b0b-121">-DefaultProfile</span></span>
<span data-ttu-id="a3b0b-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b0b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3b0b-123">-ResourceId</span></span>
<span data-ttu-id="a3b0b-124">Identificador de recursos ARM de um esquema de API.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="a3b0b-125">Se especificado, tentará localizar o esquema de API pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="a3b0b-126">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-126">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3b0b-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="a3b0b-127">-SchemaId</span></span>
<span data-ttu-id="a3b0b-128">O identificador do esquema.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-128">The identifier of the Schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b0b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b0b-129">CommonParameters</span></span>
<span data-ttu-id="a3b0b-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b0b-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3b0b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b0b-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3b0b-132">INPUTS</span></span>

### <span data-ttu-id="a3b0b-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a3b0b-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a3b0b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a3b0b-134">System.String</span></span>

## <span data-ttu-id="a3b0b-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3b0b-135">OUTPUTS</span></span>

### <span data-ttu-id="a3b0b-136">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a3b0b-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="a3b0b-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3b0b-137">NOTES</span></span>

## <span data-ttu-id="a3b0b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3b0b-138">RELATED LINKS</span></span>

[<span data-ttu-id="a3b0b-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a3b0b-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="a3b0b-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a3b0b-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="a3b0b-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a3b0b-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)