---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 8c6bc7a9e29d6f187285cacdc9df3621fcba8d0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111226"
---
# <span data-ttu-id="ca1f9-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ca1f9-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="ca1f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ca1f9-103">Exclui uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="ca1f9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca1f9-104">SYNTAX</span></span>

### <span data-ttu-id="ca1f9-105">ExpandedParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ca1f9-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca1f9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ca1f9-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca1f9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ca1f9-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca1f9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca1f9-108">DESCRIPTION</span></span>
<span data-ttu-id="ca1f9-109">O cmdlet **Remove-AzApiManagementSubscription** exclui uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="ca1f9-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca1f9-110">EXAMPLES</span></span>

### <span data-ttu-id="ca1f9-111">Exemplo 1: Excluir uma assinatura</span><span class="sxs-lookup"><span data-stu-id="ca1f9-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="ca1f9-112">Esse comando exclui uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="ca1f9-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca1f9-113">PARAMETERS</span></span>

### <span data-ttu-id="ca1f9-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ca1f9-114">-Context</span></span>
<span data-ttu-id="ca1f9-115">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="ca1f9-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca1f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca1f9-116">-DefaultProfile</span></span>
<span data-ttu-id="ca1f9-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca1f9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca1f9-118">-InputObject</span></span>
<span data-ttu-id="ca1f9-119">Instância de PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="ca1f9-120">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca1f9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca1f9-121">-PassThru</span></span>
<span data-ttu-id="ca1f9-122">Indica que esse cmdlet retorna um valor de $True, se for bem-sucedido, ou um valor de $false, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca1f9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca1f9-123">-ResourceId</span></span>
<span data-ttu-id="ca1f9-124">Arm ResourceId of Subscription.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="ca1f9-125">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca1f9-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca1f9-126">-SubscriptionId</span></span>
<span data-ttu-id="ca1f9-127">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="ca1f9-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ca1f9-128">-Confirm</span></span>
<span data-ttu-id="ca1f9-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1f9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca1f9-130">-WhatIf</span></span>
<span data-ttu-id="ca1f9-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca1f9-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca1f9-133">CommonParameters</span></span>
<span data-ttu-id="ca1f9-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca1f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca1f9-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca1f9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca1f9-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="ca1f9-136">INPUTS</span></span>

### <span data-ttu-id="ca1f9-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ca1f9-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ca1f9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ca1f9-138">System.String</span></span>

### <span data-ttu-id="ca1f9-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ca1f9-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ca1f9-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="ca1f9-140">OUTPUTS</span></span>

### <span data-ttu-id="ca1f9-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca1f9-141">System.Boolean</span></span>

## <span data-ttu-id="ca1f9-142">Notas</span><span class="sxs-lookup"><span data-stu-id="ca1f9-142">NOTES</span></span>

## <span data-ttu-id="ca1f9-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca1f9-143">RELATED LINKS</span></span>

[<span data-ttu-id="ca1f9-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ca1f9-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="ca1f9-145">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ca1f9-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="ca1f9-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ca1f9-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


