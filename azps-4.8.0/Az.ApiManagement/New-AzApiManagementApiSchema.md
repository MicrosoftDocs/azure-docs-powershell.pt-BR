---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7714c9118364f0d2ecc6e8773983acb916702281
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955181"
---
# <span data-ttu-id="1caeb-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="1caeb-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="1caeb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1caeb-102">SYNOPSIS</span></span>
<span data-ttu-id="1caeb-103">Cria o novo esquema de API no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1caeb-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="1caeb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1caeb-104">SYNTAX</span></span>

### <span data-ttu-id="1caeb-105">SchemaDocumentInline (padrão)</span><span class="sxs-lookup"><span data-stu-id="1caeb-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1caeb-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="1caeb-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1caeb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1caeb-107">DESCRIPTION</span></span>
<span data-ttu-id="1caeb-108">Cria o novo esquema de API da API.</span><span class="sxs-lookup"><span data-stu-id="1caeb-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="1caeb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1caeb-109">EXAMPLES</span></span>

### <span data-ttu-id="1caeb-110">Exemplo 1: criar um novo esquema para a API Swagger petstore extensa</span><span class="sxs-lookup"><span data-stu-id="1caeb-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="1caeb-111">O cmdlet **New-AzApiManagementApiSchema** cria ou atualiza o esquema da `swagger-petstore-extensive` aPI.</span><span class="sxs-lookup"><span data-stu-id="1caeb-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="1caeb-112">OS</span><span class="sxs-lookup"><span data-stu-id="1caeb-112">PARAMETERS</span></span>

### <span data-ttu-id="1caeb-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1caeb-113">-ApiId</span></span>
<span data-ttu-id="1caeb-114">Identificador de API.</span><span class="sxs-lookup"><span data-stu-id="1caeb-114">Identifier of api.</span></span> <span data-ttu-id="1caeb-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1caeb-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1caeb-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1caeb-116">-Context</span></span>
<span data-ttu-id="1caeb-117">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1caeb-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1caeb-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1caeb-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1caeb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1caeb-119">-DefaultProfile</span></span>
<span data-ttu-id="1caeb-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1caeb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1caeb-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="1caeb-121">-SchemaDocument</span></span>
<span data-ttu-id="1caeb-122">Documento de esquema de API como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1caeb-122">Api schema document as a string.</span></span> <span data-ttu-id="1caeb-123">Esse parâmetro é obrigatório porque-SchemaDocumentFile não está especificado.</span><span class="sxs-lookup"><span data-stu-id="1caeb-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentInline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1caeb-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="1caeb-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="1caeb-125">ContentType do esquema de API.</span><span class="sxs-lookup"><span data-stu-id="1caeb-125">ContentType of the api Schema.</span></span> <span data-ttu-id="1caeb-126">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1caeb-126">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1caeb-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="1caeb-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="1caeb-128">Caminho do arquivo de documento do esquema de API.</span><span class="sxs-lookup"><span data-stu-id="1caeb-128">Api schema document file path.</span></span> <span data-ttu-id="1caeb-129">Esse parâmetro é obrigatório porque-SchemaDocument não está especificado.</span><span class="sxs-lookup"><span data-stu-id="1caeb-129">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1caeb-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="1caeb-130">-SchemaId</span></span>
<span data-ttu-id="1caeb-131">Identificador do novo esquema.</span><span class="sxs-lookup"><span data-stu-id="1caeb-131">Identifier of new schema.</span></span>
<span data-ttu-id="1caeb-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1caeb-132">This parameter is optional.</span></span>
<span data-ttu-id="1caeb-133">Se não for especificado, será gerado.</span><span class="sxs-lookup"><span data-stu-id="1caeb-133">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1caeb-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1caeb-134">-Confirm</span></span>
<span data-ttu-id="1caeb-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1caeb-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1caeb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1caeb-136">-WhatIf</span></span>
<span data-ttu-id="1caeb-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1caeb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1caeb-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1caeb-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1caeb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1caeb-139">CommonParameters</span></span>
<span data-ttu-id="1caeb-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1caeb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1caeb-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1caeb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1caeb-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1caeb-142">INPUTS</span></span>

### <span data-ttu-id="1caeb-143">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1caeb-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1caeb-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1caeb-144">System.String</span></span>

## <span data-ttu-id="1caeb-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1caeb-145">OUTPUTS</span></span>

### <span data-ttu-id="1caeb-146">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="1caeb-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="1caeb-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1caeb-147">NOTES</span></span>

## <span data-ttu-id="1caeb-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1caeb-148">RELATED LINKS</span></span>

[<span data-ttu-id="1caeb-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="1caeb-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="1caeb-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="1caeb-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="1caeb-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="1caeb-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
