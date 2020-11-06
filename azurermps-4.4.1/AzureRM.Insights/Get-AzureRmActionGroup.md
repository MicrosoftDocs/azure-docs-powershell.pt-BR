---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
ms.openlocfilehash: 4edb403452d262705fe8fa61691ac77ba4524977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441052"
---
# <span data-ttu-id="ba235-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="ba235-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="ba235-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba235-102">SYNOPSIS</span></span>
<span data-ttu-id="ba235-103">Obtém grupo (s) de ação.</span><span class="sxs-lookup"><span data-stu-id="ba235-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba235-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba235-104">SYNTAX</span></span>

### <span data-ttu-id="ba235-105">BySubscriptionOrResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="ba235-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba235-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ba235-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba235-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba235-107">DESCRIPTION</span></span>
<span data-ttu-id="ba235-108">O cmdlet **Get-AzureRmActionGroup** Obtém um ou mais grupos de ações.</span><span class="sxs-lookup"><span data-stu-id="ba235-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="ba235-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba235-109">EXAMPLES</span></span>

### <span data-ttu-id="ba235-110">Exemplo 1: obter um grupo de ação por ID de assinatura</span><span class="sxs-lookup"><span data-stu-id="ba235-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="ba235-111">Esse comando lista todo o grupo de ação para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ba235-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="ba235-112">Exemplo 2: obter grupos de ações para o grupo de recursos específico</span><span class="sxs-lookup"><span data-stu-id="ba235-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="ba235-113">Este comando lista os grupos de ações para o grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="ba235-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="ba235-114">Exemplo 3: obter um grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="ba235-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="ba235-115">Esse comando lista um grupo de ação (um lista com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="ba235-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="ba235-116">OS</span><span class="sxs-lookup"><span data-stu-id="ba235-116">PARAMETERS</span></span>

### <span data-ttu-id="ba235-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba235-117">-Name</span></span>
<span data-ttu-id="ba235-118">O nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="ba235-118">The name of the action group.</span></span>

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

### <span data-ttu-id="ba235-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba235-119">-DefaultProfile</span></span>
<span data-ttu-id="ba235-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba235-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba235-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba235-121">-ResourceGroupName</span></span>
<span data-ttu-id="ba235-122">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ba235-122">The resource group name</span></span>

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

### <span data-ttu-id="ba235-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba235-123">CommonParameters</span></span>
<span data-ttu-id="ba235-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba235-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba235-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba235-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba235-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba235-126">INPUTS</span></span>

### <span data-ttu-id="ba235-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ba235-127">None</span></span>

## <span data-ttu-id="ba235-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba235-128">OUTPUTS</span></span>

### <span data-ttu-id="ba235-129"><System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupResource]</span><span class="sxs-lookup"><span data-stu-id="ba235-129"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource]</span></span>

### <span data-ttu-id="ba235-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ba235-130">None</span></span>

## <span data-ttu-id="ba235-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba235-131">NOTES</span></span>

## <span data-ttu-id="ba235-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba235-132">RELATED LINKS</span></span>

<span data-ttu-id="ba235-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="ba235-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
