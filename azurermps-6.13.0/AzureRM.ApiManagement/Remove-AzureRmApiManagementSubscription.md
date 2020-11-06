---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 09a0af4685701de60fc85c1572b492e7582ff71e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609448"
---
# <span data-ttu-id="73cc3-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="73cc3-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="73cc3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="73cc3-103">Exclui uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="73cc3-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73cc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73cc3-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73cc3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73cc3-105">DESCRIPTION</span></span>
<span data-ttu-id="73cc3-106">O cmdlet **Remove-AzureRmApiManagementSubscription** exclui uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="73cc3-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="73cc3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73cc3-107">EXAMPLES</span></span>

### <span data-ttu-id="73cc3-108">Exemplo 1: excluir uma assinatura</span><span class="sxs-lookup"><span data-stu-id="73cc3-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="73cc3-109">Este comando exclui uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="73cc3-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="73cc3-110">OS</span><span class="sxs-lookup"><span data-stu-id="73cc3-110">PARAMETERS</span></span>

### <span data-ttu-id="73cc3-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="73cc3-111">-Context</span></span>
<span data-ttu-id="73cc3-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="73cc3-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="73cc3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73cc3-113">-DefaultProfile</span></span>
<span data-ttu-id="73cc3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73cc3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73cc3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73cc3-115">-PassThru</span></span>
<span data-ttu-id="73cc3-116">Indica que esse cmdlet retorna um valor de $True, se tiver êxito, ou um valor de $false, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="73cc3-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="73cc3-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73cc3-117">-SubscriptionId</span></span>
<span data-ttu-id="73cc3-118">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="73cc3-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="73cc3-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="73cc3-119">-Confirm</span></span>
<span data-ttu-id="73cc3-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73cc3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73cc3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73cc3-121">-WhatIf</span></span>
<span data-ttu-id="73cc3-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73cc3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73cc3-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73cc3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73cc3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73cc3-124">CommonParameters</span></span>
<span data-ttu-id="73cc3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73cc3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73cc3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73cc3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73cc3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73cc3-127">INPUTS</span></span>

### <span data-ttu-id="73cc3-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="73cc3-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="73cc3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="73cc3-129">System.String</span></span>

### <span data-ttu-id="73cc3-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="73cc3-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="73cc3-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73cc3-131">OUTPUTS</span></span>

### <span data-ttu-id="73cc3-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73cc3-132">System.Boolean</span></span>

## <span data-ttu-id="73cc3-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73cc3-133">NOTES</span></span>

## <span data-ttu-id="73cc3-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73cc3-134">RELATED LINKS</span></span>

[<span data-ttu-id="73cc3-135">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="73cc3-135">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="73cc3-136">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="73cc3-136">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="73cc3-137">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="73cc3-137">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


