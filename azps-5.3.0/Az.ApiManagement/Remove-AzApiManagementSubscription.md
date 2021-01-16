---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 8c6bc7a9e29d6f187285cacdc9df3621fcba8d0f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272140"
---
# <span data-ttu-id="46937-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="46937-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="46937-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46937-102">SYNOPSIS</span></span>
<span data-ttu-id="46937-103">Exclui uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="46937-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="46937-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46937-104">SYNTAX</span></span>

### <span data-ttu-id="46937-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="46937-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46937-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="46937-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46937-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="46937-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46937-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46937-108">DESCRIPTION</span></span>
<span data-ttu-id="46937-109">O cmdlet **Remove-AzApiManagementSubscription** exclui uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="46937-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="46937-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46937-110">EXAMPLES</span></span>

### <span data-ttu-id="46937-111">Exemplo 1: excluir uma assinatura</span><span class="sxs-lookup"><span data-stu-id="46937-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="46937-112">Este comando exclui uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="46937-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="46937-113">OS</span><span class="sxs-lookup"><span data-stu-id="46937-113">PARAMETERS</span></span>

### <span data-ttu-id="46937-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="46937-114">-Context</span></span>
<span data-ttu-id="46937-115">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="46937-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="46937-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46937-116">-DefaultProfile</span></span>
<span data-ttu-id="46937-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46937-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46937-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46937-118">-InputObject</span></span>
<span data-ttu-id="46937-119">Instância do PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="46937-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="46937-120">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="46937-120">This parameter is required.</span></span>

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

### <span data-ttu-id="46937-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46937-121">-PassThru</span></span>
<span data-ttu-id="46937-122">Indica que esse cmdlet retorna um valor de $True, se tiver êxito, ou um valor de $false, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="46937-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="46937-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46937-123">-ResourceId</span></span>
<span data-ttu-id="46937-124">Resourcebinding da assinatura.</span><span class="sxs-lookup"><span data-stu-id="46937-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="46937-125">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="46937-125">This parameter is required.</span></span>

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

### <span data-ttu-id="46937-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46937-126">-SubscriptionId</span></span>
<span data-ttu-id="46937-127">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="46937-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="46937-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="46937-128">-Confirm</span></span>
<span data-ttu-id="46937-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46937-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46937-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46937-130">-WhatIf</span></span>
<span data-ttu-id="46937-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46937-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46937-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46937-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46937-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46937-133">CommonParameters</span></span>
<span data-ttu-id="46937-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46937-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46937-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46937-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46937-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46937-136">INPUTS</span></span>

### <span data-ttu-id="46937-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="46937-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="46937-138">System. String</span><span class="sxs-lookup"><span data-stu-id="46937-138">System.String</span></span>

### <span data-ttu-id="46937-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="46937-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="46937-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46937-140">OUTPUTS</span></span>

### <span data-ttu-id="46937-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46937-141">System.Boolean</span></span>

## <span data-ttu-id="46937-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46937-142">NOTES</span></span>

## <span data-ttu-id="46937-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46937-143">RELATED LINKS</span></span>

[<span data-ttu-id="46937-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="46937-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="46937-145">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="46937-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="46937-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="46937-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


