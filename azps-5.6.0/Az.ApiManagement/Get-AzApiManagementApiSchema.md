---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 3af651595ba51f7e5443a9f6447d07848470dc90
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886505"
---
# <span data-ttu-id="32227-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="32227-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="32227-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32227-102">SYNOPSIS</span></span>
<span data-ttu-id="32227-103">Obter os detalhes do esquema da API</span><span class="sxs-lookup"><span data-stu-id="32227-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="32227-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="32227-104">SYNTAX</span></span>

### <span data-ttu-id="32227-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="32227-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32227-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32227-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32227-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="32227-107">DESCRIPTION</span></span>
<span data-ttu-id="32227-108">O cmdlet **Get-AzApiManagementApiSchema** obtém os detalhes do Esquema de API</span><span class="sxs-lookup"><span data-stu-id="32227-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="32227-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32227-109">EXAMPLES</span></span>

### <span data-ttu-id="32227-110">Exemplo 1: Obter os detalhes de todo o Esquema de Api de uma Api</span><span class="sxs-lookup"><span data-stu-id="32227-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
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

<span data-ttu-id="32227-111">Este comando obtém todos os esquemas de API associados a uma Api `swagger-petstore-extensive` para contexto de ApiManagement específico.</span><span class="sxs-lookup"><span data-stu-id="32227-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="32227-112">Exemplo 2: Obter o esquema específico associado a uma Api</span><span class="sxs-lookup"><span data-stu-id="32227-112">Example 2: Get the specific schema associated with an Api</span></span>
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

<span data-ttu-id="32227-113">Este comando obtém o esquema de API `5cc9cf67e6ed3b1154e638bd` associado a uma Api para o Contexto de `swagger-petstore-extensive` ApiManagement específico.</span><span class="sxs-lookup"><span data-stu-id="32227-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="32227-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="32227-114">PARAMETERS</span></span>

### <span data-ttu-id="32227-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="32227-115">-ApiId</span></span>
<span data-ttu-id="32227-116">Identificador de API a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="32227-116">API identifier to look for.</span></span>
<span data-ttu-id="32227-117">Se especificado, tentará obter a API pela Id.</span><span class="sxs-lookup"><span data-stu-id="32227-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="32227-118">-Context</span><span class="sxs-lookup"><span data-stu-id="32227-118">-Context</span></span>
<span data-ttu-id="32227-119">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="32227-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="32227-120">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="32227-120">This parameter is required.</span></span>

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

### <span data-ttu-id="32227-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32227-121">-DefaultProfile</span></span>
<span data-ttu-id="32227-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32227-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32227-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32227-123">-ResourceId</span></span>
<span data-ttu-id="32227-124">Arm Resource Identifier of a Api Schema.</span><span class="sxs-lookup"><span data-stu-id="32227-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="32227-125">Se especificado, tentará encontrar o esquema de api pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="32227-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="32227-126">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="32227-126">This parameter is required.</span></span>

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

### <span data-ttu-id="32227-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="32227-127">-SchemaId</span></span>
<span data-ttu-id="32227-128">O identificador do Esquema.</span><span class="sxs-lookup"><span data-stu-id="32227-128">The identifier of the Schema.</span></span>

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

### <span data-ttu-id="32227-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32227-129">CommonParameters</span></span>
<span data-ttu-id="32227-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32227-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32227-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32227-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32227-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32227-132">INPUTS</span></span>

### <span data-ttu-id="32227-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="32227-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="32227-134">System.String</span><span class="sxs-lookup"><span data-stu-id="32227-134">System.String</span></span>

## <span data-ttu-id="32227-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="32227-135">OUTPUTS</span></span>

### <span data-ttu-id="32227-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="32227-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="32227-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="32227-137">NOTES</span></span>

## <span data-ttu-id="32227-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32227-138">RELATED LINKS</span></span>

[<span data-ttu-id="32227-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="32227-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="32227-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="32227-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="32227-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="32227-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)