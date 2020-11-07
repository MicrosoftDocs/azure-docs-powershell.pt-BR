---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 411fa67d81b772c2e9dcd6b1690e8eac50de3ea0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771363"
---
# <span data-ttu-id="b551b-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b551b-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="b551b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b551b-102">SYNOPSIS</span></span>
<span data-ttu-id="b551b-103">Exclui uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="b551b-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="b551b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b551b-104">SYNTAX</span></span>

```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b551b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b551b-105">DESCRIPTION</span></span>
<span data-ttu-id="b551b-106">O cmdlet **Remove-AzApiManagementSubscription** exclui uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="b551b-106">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="b551b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b551b-107">EXAMPLES</span></span>

### <span data-ttu-id="b551b-108">Exemplo 1: excluir uma assinatura</span><span class="sxs-lookup"><span data-stu-id="b551b-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="b551b-109">Este comando exclui uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="b551b-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="b551b-110">OS</span><span class="sxs-lookup"><span data-stu-id="b551b-110">PARAMETERS</span></span>

### <span data-ttu-id="b551b-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b551b-111">-Context</span></span>
<span data-ttu-id="b551b-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b551b-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b551b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b551b-113">-DefaultProfile</span></span>
<span data-ttu-id="b551b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b551b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b551b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b551b-115">-PassThru</span></span>
<span data-ttu-id="b551b-116">Indica que esse cmdlet retorna um valor de $True, se tiver êxito, ou um valor de $false, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b551b-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="b551b-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b551b-117">-SubscriptionId</span></span>
<span data-ttu-id="b551b-118">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="b551b-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="b551b-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b551b-119">-Confirm</span></span>
<span data-ttu-id="b551b-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b551b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b551b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b551b-121">-WhatIf</span></span>
<span data-ttu-id="b551b-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b551b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b551b-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b551b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b551b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b551b-124">CommonParameters</span></span>
<span data-ttu-id="b551b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b551b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b551b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b551b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b551b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b551b-127">INPUTS</span></span>

### <span data-ttu-id="b551b-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b551b-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b551b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b551b-129">System.String</span></span>

### <span data-ttu-id="b551b-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b551b-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b551b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b551b-131">OUTPUTS</span></span>

### <span data-ttu-id="b551b-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b551b-132">System.Boolean</span></span>

## <span data-ttu-id="b551b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b551b-133">NOTES</span></span>

## <span data-ttu-id="b551b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b551b-134">RELATED LINKS</span></span>

[<span data-ttu-id="b551b-135">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b551b-135">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="b551b-136">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b551b-136">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="b551b-137">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b551b-137">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


