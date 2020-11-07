---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 7a881b6479561ac7a616158c8054bff592209289
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786529"
---
# <span data-ttu-id="4d9dc-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="4d9dc-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="4d9dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="4d9dc-103">Obtém grupo (s) de ação.</span><span class="sxs-lookup"><span data-stu-id="4d9dc-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d9dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d9dc-104">SYNTAX</span></span>

### <span data-ttu-id="4d9dc-105">BySubscriptionOrResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="4d9dc-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d9dc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4d9dc-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d9dc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d9dc-107">DESCRIPTION</span></span>
<span data-ttu-id="4d9dc-108">O cmdlet **Get-AzureRmActionGroup** Obtém um ou mais grupos de ações.</span><span class="sxs-lookup"><span data-stu-id="4d9dc-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="4d9dc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d9dc-109">EXAMPLES</span></span>

### <span data-ttu-id="4d9dc-110">Exemplo 1: obter um grupo de ação por ID de assinatura</span><span class="sxs-lookup"><span data-stu-id="4d9dc-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="4d9dc-111">Esse comando lista todo o grupo de ação para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="4d9dc-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="4d9dc-112">Exemplo 2: obter grupos de ações para o grupo de recursos específico</span><span class="sxs-lookup"><span data-stu-id="4d9dc-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="4d9dc-113">Este comando lista os grupos de ações para o grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="4d9dc-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="4d9dc-114">Exemplo 3: obter um grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="4d9dc-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="4d9dc-115">Esse comando lista um grupo de ação (um lista com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="4d9dc-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="4d9dc-116">OS</span><span class="sxs-lookup"><span data-stu-id="4d9dc-116">PARAMETERS</span></span>

### <span data-ttu-id="4d9dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d9dc-117">-DefaultProfile</span></span>
<span data-ttu-id="4d9dc-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4d9dc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d9dc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d9dc-119">-Name</span></span>
<span data-ttu-id="4d9dc-120">O nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="4d9dc-120">The name of the action group.</span></span>

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

### <span data-ttu-id="4d9dc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d9dc-121">-ResourceGroupName</span></span>
<span data-ttu-id="4d9dc-122">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4d9dc-122">The resource group name</span></span>

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

### <span data-ttu-id="4d9dc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d9dc-123">CommonParameters</span></span>
<span data-ttu-id="4d9dc-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d9dc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d9dc-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d9dc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d9dc-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d9dc-126">INPUTS</span></span>

### <span data-ttu-id="4d9dc-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4d9dc-127">System.String</span></span>

## <span data-ttu-id="4d9dc-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d9dc-128">OUTPUTS</span></span>

### <span data-ttu-id="4d9dc-129">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="4d9dc-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="4d9dc-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d9dc-130">NOTES</span></span>

## <span data-ttu-id="4d9dc-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d9dc-131">RELATED LINKS</span></span>

<span data-ttu-id="4d9dc-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="4d9dc-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
