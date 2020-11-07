---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 26a1fbcc2016de2e6eca4cff2ee2442ef0111919
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770331"
---
# <span data-ttu-id="40b49-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="40b49-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="40b49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40b49-102">SYNOPSIS</span></span>
<span data-ttu-id="40b49-103">Obtém um ou mais recursos de alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="40b49-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="40b49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40b49-104">SYNTAX</span></span>

### <span data-ttu-id="40b49-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="40b49-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40b49-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="40b49-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40b49-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40b49-107">DESCRIPTION</span></span>
<span data-ttu-id="40b49-108">O cmdlet **Get-AzActivityLogAlert** Obtém um ou mais recursos de alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="40b49-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="40b49-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40b49-109">EXAMPLES</span></span>

### <span data-ttu-id="40b49-110">Exemplo 1: obter alertas de log de atividades por ID de assinatura</span><span class="sxs-lookup"><span data-stu-id="40b49-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="40b49-111">Esse comando lista todos os alertas de log de atividades para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="40b49-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="40b49-112">Exemplo 2: obter alertas de log de atividade para o grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="40b49-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="40b49-113">Este comando lista os alertas de log de atividades para o grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="40b49-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="40b49-114">Exemplo 3: obter um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="40b49-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="40b49-115">Esse comando lista um alerta de registro de atividades (um único elemento com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="40b49-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="40b49-116">OS</span><span class="sxs-lookup"><span data-stu-id="40b49-116">PARAMETERS</span></span>

### <span data-ttu-id="40b49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b49-117">-DefaultProfile</span></span>
<span data-ttu-id="40b49-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="40b49-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40b49-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="40b49-119">-Name</span></span>
<span data-ttu-id="40b49-120">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="40b49-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="40b49-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b49-121">-ResourceGroupName</span></span>
<span data-ttu-id="40b49-122">O nome do grupo de recursos onde existe o recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="40b49-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="40b49-123">Se o nome não for nulo ou estiver vazio, esse parâmetro deverá conter uma cadeia de caracteres não vazia.</span><span class="sxs-lookup"><span data-stu-id="40b49-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="40b49-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b49-124">CommonParameters</span></span>
<span data-ttu-id="40b49-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40b49-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b49-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40b49-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b49-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40b49-127">INPUTS</span></span>

### <span data-ttu-id="40b49-128">System. String</span><span class="sxs-lookup"><span data-stu-id="40b49-128">System.String</span></span>

## <span data-ttu-id="40b49-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40b49-129">OUTPUTS</span></span>

### <span data-ttu-id="40b49-130">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="40b49-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="40b49-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40b49-131">NOTES</span></span>

## <span data-ttu-id="40b49-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40b49-132">RELATED LINKS</span></span>

[<span data-ttu-id="40b49-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="40b49-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="40b49-134">Update-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="40b49-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="40b49-135">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="40b49-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="40b49-136">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="40b49-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="40b49-137">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="40b49-137">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)
