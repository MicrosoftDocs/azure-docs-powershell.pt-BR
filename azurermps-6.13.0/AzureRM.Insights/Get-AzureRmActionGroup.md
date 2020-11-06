---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
ms.openlocfilehash: 002847ae580e3e3c5d5b44e05ebc1633e4e1574b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602723"
---
# <span data-ttu-id="e96b4-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="e96b4-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="e96b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e96b4-102">SYNOPSIS</span></span>
<span data-ttu-id="e96b4-103">Obtém grupo (s) de ação.</span><span class="sxs-lookup"><span data-stu-id="e96b4-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e96b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e96b4-104">SYNTAX</span></span>

### <span data-ttu-id="e96b4-105">BySubscriptionOrResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="e96b4-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e96b4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e96b4-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e96b4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e96b4-107">DESCRIPTION</span></span>
<span data-ttu-id="e96b4-108">O cmdlet **Get-AzureRmActionGroup** Obtém um ou mais grupos de ações.</span><span class="sxs-lookup"><span data-stu-id="e96b4-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="e96b4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e96b4-109">EXAMPLES</span></span>

### <span data-ttu-id="e96b4-110">Exemplo 1: obter um grupo de ação por ID de assinatura</span><span class="sxs-lookup"><span data-stu-id="e96b4-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="e96b4-111">Esse comando lista todo o grupo de ação para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="e96b4-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="e96b4-112">Exemplo 2: obter grupos de ações para o grupo de recursos específico</span><span class="sxs-lookup"><span data-stu-id="e96b4-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="e96b4-113">Este comando lista os grupos de ações para o grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="e96b4-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="e96b4-114">Exemplo 3: obter um grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="e96b4-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="e96b4-115">Esse comando lista um grupo de ação (um lista com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="e96b4-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="e96b4-116">OS</span><span class="sxs-lookup"><span data-stu-id="e96b4-116">PARAMETERS</span></span>

### <span data-ttu-id="e96b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e96b4-117">-DefaultProfile</span></span>
<span data-ttu-id="e96b4-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e96b4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e96b4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e96b4-119">-Name</span></span>
<span data-ttu-id="e96b4-120">O nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="e96b4-120">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96b4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e96b4-121">-ResourceGroupName</span></span>
<span data-ttu-id="e96b4-122">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e96b4-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e96b4-123">CommonParameters</span></span>
<span data-ttu-id="e96b4-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e96b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e96b4-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e96b4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e96b4-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e96b4-126">INPUTS</span></span>

### <span data-ttu-id="e96b4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e96b4-127">System.String</span></span>

## <span data-ttu-id="e96b4-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e96b4-128">OUTPUTS</span></span>

### <span data-ttu-id="e96b4-129">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="e96b4-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="e96b4-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e96b4-130">NOTES</span></span>

## <span data-ttu-id="e96b4-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e96b4-131">RELATED LINKS</span></span>

<span data-ttu-id="e96b4-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="e96b4-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
