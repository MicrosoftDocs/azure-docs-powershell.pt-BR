---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroupSubscription.md
ms.openlocfilehash: 882583c50db8a4b4473bce829aab120a68478434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427174"
---
# <span data-ttu-id="2e8bc-101">Remove-AzureRmManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="2e8bc-101">Remove-AzureRmManagementGroupSubscription</span></span>

## <span data-ttu-id="2e8bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="2e8bc-103">Remove uma assinatura de um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="2e8bc-103">Removes a Subscription from a Management Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e8bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e8bc-104">SYNTAX</span></span>

```
Remove-AzureRmManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e8bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e8bc-105">DESCRIPTION</span></span>
<span data-ttu-id="2e8bc-106">O cmdlet **Remove-AzureRmManagementGroupSubscription** remove uma assinatura de um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="2e8bc-106">The **Remove-AzureRmManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="2e8bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e8bc-107">EXAMPLES</span></span>

### <span data-ttu-id="2e8bc-108">Exemplo 1-remover a assinatura de um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2e8bc-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="2e8bc-109">OS</span><span class="sxs-lookup"><span data-stu-id="2e8bc-109">PARAMETERS</span></span>

### <span data-ttu-id="2e8bc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e8bc-110">-DefaultProfile</span></span>
<span data-ttu-id="2e8bc-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8bc-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e8bc-112">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="2e8bc-112">-GroupName</span></span>
<span data-ttu-id="2e8bc-113">ID do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2e8bc-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8bc-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e8bc-114">-PassThru</span></span>
<span data-ttu-id="2e8bc-115">Retorno `true` sobre a execução bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="2e8bc-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="2e8bc-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e8bc-116">-SubscriptionId</span></span>
<span data-ttu-id="2e8bc-117">ID da assinatura associada ao gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2e8bc-117">Subscription Id of the subscription associated witht the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8bc-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e8bc-118">-Confirm</span></span>
<span data-ttu-id="2e8bc-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e8bc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e8bc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e8bc-120">-WhatIf</span></span>
<span data-ttu-id="2e8bc-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e8bc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e8bc-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e8bc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e8bc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e8bc-123">CommonParameters</span></span>
<span data-ttu-id="2e8bc-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e8bc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e8bc-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e8bc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e8bc-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e8bc-126">INPUTS</span></span>

### <span data-ttu-id="2e8bc-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2e8bc-127">None</span></span>

## <span data-ttu-id="2e8bc-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e8bc-128">OUTPUTS</span></span>

### <span data-ttu-id="2e8bc-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2e8bc-129">System.Boolean</span></span>

## <span data-ttu-id="2e8bc-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e8bc-130">NOTES</span></span>

## <span data-ttu-id="2e8bc-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e8bc-131">RELATED LINKS</span></span>