---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 31e36048587ba6faeee42ab1c2bf15afe1ae1e71
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398743"
---
# <span data-ttu-id="84dd2-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="84dd2-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="84dd2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="84dd2-103">Recebe um ou mais recursos de alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="84dd2-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="84dd2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84dd2-104">SYNTAX</span></span>

### <span data-ttu-id="84dd2-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="84dd2-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84dd2-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="84dd2-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84dd2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="84dd2-107">DESCRIPTION</span></span>
<span data-ttu-id="84dd2-108">O **cmdlet Get-AzActivityLogAlert** recebe um ou mais recursos de alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="84dd2-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="84dd2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="84dd2-109">EXAMPLES</span></span>

### <span data-ttu-id="84dd2-110">Exemplo 1: Obter alertas de log de atividades por ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="84dd2-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="84dd2-111">Esse comando lista todos os alertas de log de atividades da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="84dd2-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="84dd2-112">Exemplo 2: Obter alertas de log de atividades para determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="84dd2-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="84dd2-113">Esse comando lista alertas de log de atividades para o determinado grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="84dd2-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="84dd2-114">Exemplo 3: Obter um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="84dd2-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="84dd2-115">Esse comando lista um alerta de log de atividades (uma lista com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="84dd2-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="84dd2-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84dd2-116">PARAMETERS</span></span>

### <span data-ttu-id="84dd2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84dd2-117">-DefaultProfile</span></span>
<span data-ttu-id="84dd2-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="84dd2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84dd2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="84dd2-119">-Name</span></span>
<span data-ttu-id="84dd2-120">O nome do alerta do log de atividades.</span><span class="sxs-lookup"><span data-stu-id="84dd2-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84dd2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84dd2-121">-ResourceGroupName</span></span>
<span data-ttu-id="84dd2-122">O nome do grupo de recursos onde o recurso de alerta existe.</span><span class="sxs-lookup"><span data-stu-id="84dd2-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="84dd2-123">Se Nome não for nulo ou vazio, esse parâmetro deverá conter e não a cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="84dd2-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84dd2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84dd2-124">CommonParameters</span></span>
<span data-ttu-id="84dd2-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84dd2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84dd2-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84dd2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84dd2-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="84dd2-127">INPUTS</span></span>

### <span data-ttu-id="84dd2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="84dd2-128">System.String</span></span>

## <span data-ttu-id="84dd2-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="84dd2-129">OUTPUTS</span></span>

### <span data-ttu-id="84dd2-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="84dd2-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="84dd2-131">Notas</span><span class="sxs-lookup"><span data-stu-id="84dd2-131">NOTES</span></span>

## <span data-ttu-id="84dd2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84dd2-132">RELATED LINKS</span></span>

[<span data-ttu-id="84dd2-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="84dd2-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="84dd2-134">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="84dd2-134">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="84dd2-135">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="84dd2-135">New-AzActionGroup</span></span>](./New-AzActionGroup.md)
