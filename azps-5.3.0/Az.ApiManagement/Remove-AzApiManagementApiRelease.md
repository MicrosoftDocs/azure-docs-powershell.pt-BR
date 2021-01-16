---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 9673df14bdd0f5b7d0e946170a155231e8c4e751
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272180"
---
# <span data-ttu-id="fdba1-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fdba1-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="fdba1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdba1-102">SYNOPSIS</span></span>
<span data-ttu-id="fdba1-103">Remove uma versão de API específica</span><span class="sxs-lookup"><span data-stu-id="fdba1-103">Removes a particular API Release</span></span>

## <span data-ttu-id="fdba1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdba1-104">SYNTAX</span></span>

### <span data-ttu-id="fdba1-105">ByApiReleaseId (padrão)</span><span class="sxs-lookup"><span data-stu-id="fdba1-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdba1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fdba1-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdba1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fdba1-107">DESCRIPTION</span></span>

<span data-ttu-id="fdba1-108">O cmdlet **Remove-AzAzureRmApiManagementApiRelease** remove uma versão de API existente.</span><span class="sxs-lookup"><span data-stu-id="fdba1-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="fdba1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdba1-109">EXAMPLES</span></span>

### <span data-ttu-id="fdba1-110">Exemplo 1: remover uma versão de API</span><span class="sxs-lookup"><span data-stu-id="fdba1-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="fdba1-111">Esse comando Remove a versão da API com o ApiId e o releaseid especificados.</span><span class="sxs-lookup"><span data-stu-id="fdba1-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="fdba1-112">OS</span><span class="sxs-lookup"><span data-stu-id="fdba1-112">PARAMETERS</span></span>

### <span data-ttu-id="fdba1-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fdba1-113">-ApiId</span></span>
<span data-ttu-id="fdba1-114">Identificador da API.</span><span class="sxs-lookup"><span data-stu-id="fdba1-114">Identifier of the API.</span></span>
<span data-ttu-id="fdba1-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="fdba1-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdba1-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="fdba1-116">-Context</span></span>
<span data-ttu-id="fdba1-117">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fdba1-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fdba1-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="fdba1-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdba1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdba1-119">-DefaultProfile</span></span>
<span data-ttu-id="fdba1-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdba1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdba1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdba1-121">-InputObject</span></span>
<span data-ttu-id="fdba1-122">Instância do PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="fdba1-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="fdba1-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="fdba1-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdba1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdba1-124">-PassThru</span></span>
<span data-ttu-id="fdba1-125">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fdba1-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="fdba1-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="fdba1-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="fdba1-127">-Rereleaseid</span><span class="sxs-lookup"><span data-stu-id="fdba1-127">-ReleaseId</span></span>
<span data-ttu-id="fdba1-128">Identificador da versão da API.</span><span class="sxs-lookup"><span data-stu-id="fdba1-128">Identifier of the API Release.</span></span>
<span data-ttu-id="fdba1-129">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="fdba1-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdba1-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fdba1-130">-Confirm</span></span>
<span data-ttu-id="fdba1-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdba1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdba1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdba1-132">-WhatIf</span></span>
<span data-ttu-id="fdba1-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fdba1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdba1-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fdba1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdba1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdba1-135">CommonParameters</span></span>
<span data-ttu-id="fdba1-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdba1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdba1-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdba1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdba1-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fdba1-138">INPUTS</span></span>

### <span data-ttu-id="fdba1-139">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fdba1-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fdba1-140">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fdba1-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="fdba1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fdba1-141">System.String</span></span>

## <span data-ttu-id="fdba1-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fdba1-142">OUTPUTS</span></span>

### <span data-ttu-id="fdba1-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fdba1-143">System.Boolean</span></span>

## <span data-ttu-id="fdba1-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fdba1-144">NOTES</span></span>

## <span data-ttu-id="fdba1-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdba1-145">RELATED LINKS</span></span>

[<span data-ttu-id="fdba1-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fdba1-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="fdba1-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fdba1-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="fdba1-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fdba1-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)