---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 837494b8f042d3ea788eda69d47845b02859c805
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114854"
---
# <span data-ttu-id="821f4-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="821f4-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="821f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="821f4-102">SYNOPSIS</span></span>
<span data-ttu-id="821f4-103">Obter os detalhes do esquema da API</span><span class="sxs-lookup"><span data-stu-id="821f4-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="821f4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="821f4-104">SYNTAX</span></span>

### <span data-ttu-id="821f4-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="821f4-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="821f4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="821f4-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="821f4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="821f4-107">DESCRIPTION</span></span>
<span data-ttu-id="821f4-108">O cmdlet **Get-AzApiManagementApiSchema** obtém os detalhes do Esquema da API</span><span class="sxs-lookup"><span data-stu-id="821f4-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="821f4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="821f4-109">EXAMPLES</span></span>

### <span data-ttu-id="821f4-110">Exemplo 1: Obter os detalhes de todo o Esquema de Api de uma Api</span><span class="sxs-lookup"><span data-stu-id="821f4-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
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

<span data-ttu-id="821f4-111">Esse comando obtém todos os esquemas de API associados a uma Api `swagger-petstore-extensive` para contexto de ApiManagement específico.</span><span class="sxs-lookup"><span data-stu-id="821f4-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="821f4-112">Exemplo 2: Obter o esquema específico associado a uma Api</span><span class="sxs-lookup"><span data-stu-id="821f4-112">Example 2: Get the specific schema associated with an Api</span></span>
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

<span data-ttu-id="821f4-113">Esse comando obtém o esquema de API `5cc9cf67e6ed3b1154e638bd` associado a uma Api para contexto `swagger-petstore-extensive` apiManagement específico.</span><span class="sxs-lookup"><span data-stu-id="821f4-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="821f4-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="821f4-114">PARAMETERS</span></span>

### <span data-ttu-id="821f4-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="821f4-115">-ApiId</span></span>
<span data-ttu-id="821f4-116">Identificador de API a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="821f4-116">API identifier to look for.</span></span>
<span data-ttu-id="821f4-117">Se especificado, você tentará obter a API pela ID.</span><span class="sxs-lookup"><span data-stu-id="821f4-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="821f4-118">-Contexto</span><span class="sxs-lookup"><span data-stu-id="821f4-118">-Context</span></span>
<span data-ttu-id="821f4-119">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="821f4-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="821f4-120">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="821f4-120">This parameter is required.</span></span>

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

### <span data-ttu-id="821f4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="821f4-121">-DefaultProfile</span></span>
<span data-ttu-id="821f4-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="821f4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="821f4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="821f4-123">-ResourceId</span></span>
<span data-ttu-id="821f4-124">Identificador de Recurso Arm de um Esquema de Api.</span><span class="sxs-lookup"><span data-stu-id="821f4-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="821f4-125">Se especificado, tentará encontrar o esquema de api pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="821f4-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="821f4-126">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="821f4-126">This parameter is required.</span></span>

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

### <span data-ttu-id="821f4-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="821f4-127">-SchemaId</span></span>
<span data-ttu-id="821f4-128">O identificador do Esquema.</span><span class="sxs-lookup"><span data-stu-id="821f4-128">The identifier of the Schema.</span></span>

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

### <span data-ttu-id="821f4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="821f4-129">CommonParameters</span></span>
<span data-ttu-id="821f4-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="821f4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="821f4-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="821f4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="821f4-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="821f4-132">INPUTS</span></span>

### <span data-ttu-id="821f4-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="821f4-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="821f4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="821f4-134">System.String</span></span>

## <span data-ttu-id="821f4-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="821f4-135">OUTPUTS</span></span>

### <span data-ttu-id="821f4-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="821f4-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="821f4-137">Notas</span><span class="sxs-lookup"><span data-stu-id="821f4-137">NOTES</span></span>

## <span data-ttu-id="821f4-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="821f4-138">RELATED LINKS</span></span>

[<span data-ttu-id="821f4-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="821f4-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="821f4-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="821f4-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="821f4-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="821f4-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)