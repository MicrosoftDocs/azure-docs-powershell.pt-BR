---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
ms.openlocfilehash: fb144bfa228b07501c374f054970d1e3e0337ec1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93945069"
---
# <span data-ttu-id="364c6-101">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="364c6-101">Remove-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="364c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="364c6-102">SYNOPSIS</span></span>
<span data-ttu-id="364c6-103">Remove o esquema de API da API.</span><span class="sxs-lookup"><span data-stu-id="364c6-103">Removes the API Schema from the API.</span></span>

## <span data-ttu-id="364c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="364c6-104">SYNTAX</span></span>

### <span data-ttu-id="364c6-105">ByApiSchemaId (padrão)</span><span class="sxs-lookup"><span data-stu-id="364c6-105">ByApiSchemaId (Default)</span></span>
```
Remove-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="364c6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="364c6-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="364c6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="364c6-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementApiSchema -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="364c6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="364c6-108">DESCRIPTION</span></span>
<span data-ttu-id="364c6-109">O cmdlet **Remove-AzApiManagementSchema** da API.</span><span class="sxs-lookup"><span data-stu-id="364c6-109">The cmdlet **Remove-AzApiManagementSchema** from the Api.</span></span>

## <span data-ttu-id="364c6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="364c6-110">EXAMPLES</span></span>

### <span data-ttu-id="364c6-111">Exemplo 1: Remove o esquema de API da API</span><span class="sxs-lookup"><span data-stu-id="364c6-111">Example 1 : Removes the Api Schema from the API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiSchema -Context $apimContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="364c6-112">O script remove o esquema `2` da API `echo-api` se não for referenciado.</span><span class="sxs-lookup"><span data-stu-id="364c6-112">The script removes the Schema `2` from the Api `echo-api` if it is not referenced.</span></span>

## <span data-ttu-id="364c6-113">OS</span><span class="sxs-lookup"><span data-stu-id="364c6-113">PARAMETERS</span></span>

### <span data-ttu-id="364c6-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="364c6-114">-ApiId</span></span>
<span data-ttu-id="364c6-115">Identificador da API.</span><span class="sxs-lookup"><span data-stu-id="364c6-115">Identifier of the API.</span></span>
<span data-ttu-id="364c6-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="364c6-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="364c6-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="364c6-117">-Context</span></span>
<span data-ttu-id="364c6-118">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="364c6-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="364c6-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="364c6-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="364c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364c6-120">-DefaultProfile</span></span>
<span data-ttu-id="364c6-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="364c6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="364c6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="364c6-122">-InputObject</span></span>
<span data-ttu-id="364c6-123">Instância do PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="364c6-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="364c6-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="364c6-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="364c6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="364c6-125">-PassThru</span></span>
<span data-ttu-id="364c6-126">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="364c6-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="364c6-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="364c6-127">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="364c6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="364c6-128">-ResourceId</span></span>
<span data-ttu-id="364c6-129">Resourcebinding de ApiSchema.</span><span class="sxs-lookup"><span data-stu-id="364c6-129">Arm ResourceId of ApiSchema.</span></span> <span data-ttu-id="364c6-130">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="364c6-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="364c6-131">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="364c6-131">-SchemaId</span></span>
<span data-ttu-id="364c6-132">Identificador do esquema de API.</span><span class="sxs-lookup"><span data-stu-id="364c6-132">Identifier of the API Schema.</span></span>
<span data-ttu-id="364c6-133">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="364c6-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="364c6-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="364c6-134">-Confirm</span></span>
<span data-ttu-id="364c6-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="364c6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="364c6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="364c6-136">-WhatIf</span></span>
<span data-ttu-id="364c6-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="364c6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="364c6-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="364c6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="364c6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364c6-139">CommonParameters</span></span>
<span data-ttu-id="364c6-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="364c6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364c6-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="364c6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364c6-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="364c6-142">INPUTS</span></span>

### <span data-ttu-id="364c6-143">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="364c6-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="364c6-144">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="364c6-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="364c6-145">System. String</span><span class="sxs-lookup"><span data-stu-id="364c6-145">System.String</span></span>

## <span data-ttu-id="364c6-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="364c6-146">OUTPUTS</span></span>

### <span data-ttu-id="364c6-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="364c6-147">System.Boolean</span></span>

## <span data-ttu-id="364c6-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="364c6-148">NOTES</span></span>

## <span data-ttu-id="364c6-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="364c6-149">RELATED LINKS</span></span>

[<span data-ttu-id="364c6-150">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="364c6-150">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="364c6-151">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="364c6-151">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="364c6-152">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="364c6-152">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
