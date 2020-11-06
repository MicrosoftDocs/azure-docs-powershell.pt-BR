---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 71256ab72d8c5c6042aa6c17b184066f96b3a813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426505"
---
# <span data-ttu-id="9bb16-101">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9bb16-101">Remove-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="9bb16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bb16-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb16-103">Remove uma versão de API específica</span><span class="sxs-lookup"><span data-stu-id="9bb16-103">Removes a particular API Release</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bb16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bb16-104">SYNTAX</span></span>

### <span data-ttu-id="9bb16-105">ByApiReleaseId (padrão)</span><span class="sxs-lookup"><span data-stu-id="9bb16-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bb16-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9bb16-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bb16-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9bb16-107">DESCRIPTION</span></span>

<span data-ttu-id="9bb16-108">O cmdlet **Remove-AzureRmApiManagementApiRelease** remove uma versão de API existente.</span><span class="sxs-lookup"><span data-stu-id="9bb16-108">The **Remove-AzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="9bb16-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bb16-109">EXAMPLES</span></span>

### <span data-ttu-id="9bb16-110">Exemplo 1: remover uma versão de API</span><span class="sxs-lookup"><span data-stu-id="9bb16-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="9bb16-111">Esse comando Remove a versão da API com o ApiId e o releaseid especificados.</span><span class="sxs-lookup"><span data-stu-id="9bb16-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="9bb16-112">OS</span><span class="sxs-lookup"><span data-stu-id="9bb16-112">PARAMETERS</span></span>

### <span data-ttu-id="9bb16-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9bb16-113">-ApiId</span></span>
<span data-ttu-id="9bb16-114">Identificador da API.</span><span class="sxs-lookup"><span data-stu-id="9bb16-114">Identifier of the API.</span></span>
<span data-ttu-id="9bb16-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9bb16-115">This parameter is required.</span></span>

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

### <span data-ttu-id="9bb16-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9bb16-116">-Context</span></span>
<span data-ttu-id="9bb16-117">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9bb16-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9bb16-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9bb16-118">This parameter is required.</span></span>

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

### <span data-ttu-id="9bb16-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb16-119">-DefaultProfile</span></span>
<span data-ttu-id="9bb16-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb16-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb16-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bb16-121">-InputObject</span></span>
<span data-ttu-id="9bb16-122">Instância do PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="9bb16-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="9bb16-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9bb16-123">This parameter is required.</span></span>

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

### <span data-ttu-id="9bb16-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bb16-124">-PassThru</span></span>
<span data-ttu-id="9bb16-125">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9bb16-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="9bb16-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9bb16-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="9bb16-127">-Rereleaseid</span><span class="sxs-lookup"><span data-stu-id="9bb16-127">-ReleaseId</span></span>
<span data-ttu-id="9bb16-128">Identificador da versão da API.</span><span class="sxs-lookup"><span data-stu-id="9bb16-128">Identifier of the API Release.</span></span>
<span data-ttu-id="9bb16-129">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9bb16-129">This parameter is required.</span></span>

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

### <span data-ttu-id="9bb16-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9bb16-130">-Confirm</span></span>
<span data-ttu-id="9bb16-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bb16-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bb16-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bb16-132">-WhatIf</span></span>
<span data-ttu-id="9bb16-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9bb16-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bb16-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9bb16-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bb16-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb16-135">CommonParameters</span></span>
<span data-ttu-id="9bb16-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bb16-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb16-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bb16-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb16-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9bb16-138">INPUTS</span></span>

### <span data-ttu-id="9bb16-139">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9bb16-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9bb16-140">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9bb16-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>
<span data-ttu-id="9bb16-141">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9bb16-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9bb16-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9bb16-142">System.String</span></span>

## <span data-ttu-id="9bb16-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9bb16-143">OUTPUTS</span></span>

### <span data-ttu-id="9bb16-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9bb16-144">System.Boolean</span></span>

## <span data-ttu-id="9bb16-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9bb16-145">NOTES</span></span>

## <span data-ttu-id="9bb16-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bb16-146">RELATED LINKS</span></span>

[<span data-ttu-id="9bb16-147">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9bb16-147">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="9bb16-148">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9bb16-148">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="9bb16-149">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9bb16-149">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
