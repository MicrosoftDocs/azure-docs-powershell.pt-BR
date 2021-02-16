---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: fe85fd3d3fd2638933097f73fdc06e6ff2b43460
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406444"
---
# <span data-ttu-id="f7723-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="f7723-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="f7723-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7723-102">SYNOPSIS</span></span>
<span data-ttu-id="f7723-103">Obtém grupos de ações.</span><span class="sxs-lookup"><span data-stu-id="f7723-103">Gets action group(s).</span></span>

## <span data-ttu-id="f7723-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7723-104">SYNTAX</span></span>

### <span data-ttu-id="f7723-105">BySubscriptionOrResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f7723-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7723-106">Por Nome</span><span class="sxs-lookup"><span data-stu-id="f7723-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7723-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7723-107">DESCRIPTION</span></span>
<span data-ttu-id="f7723-108">O **cmdlet Get-AzActionGroup** obtém um ou mais grupos de ação.</span><span class="sxs-lookup"><span data-stu-id="f7723-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="f7723-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f7723-109">EXAMPLES</span></span>

### <span data-ttu-id="f7723-110">Exemplo 1: Obter um grupo de ações por ID de assinatura</span><span class="sxs-lookup"><span data-stu-id="f7723-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="f7723-111">Esse comando lista todo o grupo de ações da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f7723-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="f7723-112">Exemplo 2: Obter grupos de ações para o determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f7723-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="f7723-113">Esse comando lista os grupos de ações para o determinado grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7723-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="f7723-114">Exemplo 3: Obter um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="f7723-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="f7723-115">Esse comando lista um grupo de ações (uma lista com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="f7723-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="f7723-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7723-116">PARAMETERS</span></span>

### <span data-ttu-id="f7723-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7723-117">-DefaultProfile</span></span>
<span data-ttu-id="f7723-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f7723-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7723-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7723-119">-Name</span></span>
<span data-ttu-id="f7723-120">O nome do grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="f7723-120">The name of the action group.</span></span>

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

### <span data-ttu-id="f7723-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7723-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7723-122">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f7723-122">The resource group name</span></span>

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

### <span data-ttu-id="f7723-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7723-123">CommonParameters</span></span>
<span data-ttu-id="f7723-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7723-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7723-125">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7723-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7723-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="f7723-126">INPUTS</span></span>

### <span data-ttu-id="f7723-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f7723-127">System.String</span></span>

## <span data-ttu-id="f7723-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="f7723-128">OUTPUTS</span></span>

### <span data-ttu-id="f7723-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="f7723-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="f7723-130">Notas</span><span class="sxs-lookup"><span data-stu-id="f7723-130">NOTES</span></span>

## <span data-ttu-id="f7723-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7723-131">RELATED LINKS</span></span>

<span data-ttu-id="f7723-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="f7723-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
