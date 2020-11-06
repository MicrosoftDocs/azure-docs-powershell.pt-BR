---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: da277d72dfd0e1ec2a31d0727047368da100b233
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595867"
---
# <span data-ttu-id="f6ea3-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="f6ea3-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="f6ea3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ea3-103">Obtém grupo (s) de ação.</span><span class="sxs-lookup"><span data-stu-id="f6ea3-103">Gets action group(s).</span></span>

## <span data-ttu-id="f6ea3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6ea3-104">SYNTAX</span></span>

### <span data-ttu-id="f6ea3-105">BySubscriptionOrResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="f6ea3-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6ea3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f6ea3-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6ea3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6ea3-107">DESCRIPTION</span></span>
<span data-ttu-id="f6ea3-108">O cmdlet **Get-AzActionGroup** Obtém um ou mais grupos de ações.</span><span class="sxs-lookup"><span data-stu-id="f6ea3-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="f6ea3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6ea3-109">EXAMPLES</span></span>

### <span data-ttu-id="f6ea3-110">Exemplo 1: obter um grupo de ação por ID de assinatura</span><span class="sxs-lookup"><span data-stu-id="f6ea3-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="f6ea3-111">Esse comando lista todo o grupo de ação para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f6ea3-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="f6ea3-112">Exemplo 2: obter grupos de ações para o grupo de recursos específico</span><span class="sxs-lookup"><span data-stu-id="f6ea3-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="f6ea3-113">Este comando lista os grupos de ações para o grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="f6ea3-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="f6ea3-114">Exemplo 3: obter um grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="f6ea3-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="f6ea3-115">Esse comando lista um grupo de ação (um lista com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="f6ea3-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="f6ea3-116">OS</span><span class="sxs-lookup"><span data-stu-id="f6ea3-116">PARAMETERS</span></span>

### <span data-ttu-id="f6ea3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ea3-117">-DefaultProfile</span></span>
<span data-ttu-id="f6ea3-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f6ea3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6ea3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6ea3-119">-Name</span></span>
<span data-ttu-id="f6ea3-120">O nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="f6ea3-120">The name of the action group.</span></span>

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

### <span data-ttu-id="f6ea3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ea3-121">-ResourceGroupName</span></span>
<span data-ttu-id="f6ea3-122">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f6ea3-122">The resource group name</span></span>

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

### <span data-ttu-id="f6ea3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ea3-123">CommonParameters</span></span>
<span data-ttu-id="f6ea3-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6ea3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ea3-125">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6ea3-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ea3-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6ea3-126">INPUTS</span></span>

### <span data-ttu-id="f6ea3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f6ea3-127">System.String</span></span>

## <span data-ttu-id="f6ea3-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6ea3-128">OUTPUTS</span></span>

### <span data-ttu-id="f6ea3-129">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="f6ea3-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="f6ea3-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6ea3-130">NOTES</span></span>

## <span data-ttu-id="f6ea3-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6ea3-131">RELATED LINKS</span></span>

<span data-ttu-id="f6ea3-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="f6ea3-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
