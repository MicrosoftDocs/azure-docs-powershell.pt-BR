---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
ms.openlocfilehash: 2b8db6f5d550c91f806595c80be4beb300a95273
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598002"
---
# <span data-ttu-id="6325a-101">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6325a-101">Remove-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="6325a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6325a-102">SYNOPSIS</span></span>
<span data-ttu-id="6325a-103">Revisão de API específica removida</span><span class="sxs-lookup"><span data-stu-id="6325a-103">Removed a particular API Revision</span></span>

## <span data-ttu-id="6325a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6325a-104">SYNTAX</span></span>

### <span data-ttu-id="6325a-105">ByApiId (padrão)</span><span class="sxs-lookup"><span data-stu-id="6325a-105">ByApiId (Default)</span></span>
```
Remove-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6325a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6325a-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6325a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6325a-107">DESCRIPTION</span></span>
<span data-ttu-id="6325a-108">O cmdlet **Remove-AzApiManagementApiRevision** remove uma revisão de API específica.</span><span class="sxs-lookup"><span data-stu-id="6325a-108">The cmdlet **Remove-AzApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="6325a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6325a-109">EXAMPLES</span></span>

### <span data-ttu-id="6325a-110">Exemplo 1: remover uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="6325a-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="6325a-111">Esse comando Remove a `2` revisão da API `echo-api` do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="6325a-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="6325a-112">OS</span><span class="sxs-lookup"><span data-stu-id="6325a-112">PARAMETERS</span></span>

### <span data-ttu-id="6325a-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6325a-113">-ApiId</span></span>
<span data-ttu-id="6325a-114">Identificador da API.</span><span class="sxs-lookup"><span data-stu-id="6325a-114">Identifier of the API.</span></span>
<span data-ttu-id="6325a-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6325a-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6325a-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6325a-116">-ApiRevision</span></span>
<span data-ttu-id="6325a-117">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="6325a-117">Identifier of the API Revision.</span></span> <span data-ttu-id="6325a-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6325a-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6325a-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="6325a-119">-Context</span></span>
<span data-ttu-id="6325a-120">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6325a-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6325a-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6325a-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6325a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6325a-122">-DefaultProfile</span></span>
<span data-ttu-id="6325a-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6325a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6325a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6325a-124">-InputObject</span></span>
<span data-ttu-id="6325a-125">Instância do PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="6325a-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="6325a-126">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6325a-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6325a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6325a-127">-PassThru</span></span>
<span data-ttu-id="6325a-128">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6325a-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="6325a-129">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="6325a-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="6325a-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6325a-130">-Confirm</span></span>
<span data-ttu-id="6325a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6325a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6325a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6325a-132">-WhatIf</span></span>
<span data-ttu-id="6325a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6325a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6325a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6325a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6325a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6325a-135">CommonParameters</span></span>
<span data-ttu-id="6325a-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6325a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6325a-137">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6325a-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6325a-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6325a-138">INPUTS</span></span>

### <span data-ttu-id="6325a-139">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6325a-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6325a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6325a-140">System.String</span></span>

### <span data-ttu-id="6325a-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6325a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="6325a-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6325a-142">OUTPUTS</span></span>

### <span data-ttu-id="6325a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6325a-143">System.Boolean</span></span>

## <span data-ttu-id="6325a-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6325a-144">NOTES</span></span>

## <span data-ttu-id="6325a-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6325a-145">RELATED LINKS</span></span>

[<span data-ttu-id="6325a-146">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6325a-146">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="6325a-147">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6325a-147">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="6325a-148">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6325a-148">Set-AzApiManagementApiRevision</span></span>](./Set-AzApiManagementApiRevision.md)