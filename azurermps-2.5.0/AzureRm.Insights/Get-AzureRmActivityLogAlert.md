---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: af8ef3ef2662dc6793011741fdfd7a903eaa081f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786525"
---
# <span data-ttu-id="9d179-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9d179-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="9d179-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d179-102">SYNOPSIS</span></span>
<span data-ttu-id="9d179-103">Obtém um ou mais recursos de alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="9d179-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d179-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d179-104">SYNTAX</span></span>

### <span data-ttu-id="9d179-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9d179-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d179-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9d179-106">GetByResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d179-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d179-107">DESCRIPTION</span></span>
<span data-ttu-id="9d179-108">O cmdlet **Get-AzureRmActivityLogAlert** Obtém um ou mais recursos de alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="9d179-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="9d179-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d179-109">EXAMPLES</span></span>

### <span data-ttu-id="9d179-110">Exemplo 1: obter alertas de log de atividades por ID de assinatura</span><span class="sxs-lookup"><span data-stu-id="9d179-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="9d179-111">Esse comando lista todos os alertas de log de atividades para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9d179-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="9d179-112">Exemplo 2: obter alertas de log de atividade para o grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="9d179-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="9d179-113">Este comando lista os alertas de log de atividades para o grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="9d179-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="9d179-114">Exemplo 3: obter um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="9d179-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="9d179-115">Esse comando lista um alerta de registro de atividades (um único elemento com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="9d179-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="9d179-116">OS</span><span class="sxs-lookup"><span data-stu-id="9d179-116">PARAMETERS</span></span>

### <span data-ttu-id="9d179-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d179-117">-DefaultProfile</span></span>
<span data-ttu-id="9d179-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9d179-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d179-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d179-119">-Name</span></span>
<span data-ttu-id="9d179-120">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="9d179-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="9d179-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d179-121">-ResourceGroupName</span></span>
<span data-ttu-id="9d179-122">O nome do grupo de recursos onde existe o recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="9d179-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="9d179-123">Se o nome não for nulo ou estiver vazio, esse parâmetro deverá conter uma cadeia de caracteres não vazia.</span><span class="sxs-lookup"><span data-stu-id="9d179-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="9d179-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d179-124">CommonParameters</span></span>
<span data-ttu-id="9d179-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d179-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d179-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d179-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d179-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d179-127">INPUTS</span></span>

### <span data-ttu-id="9d179-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9d179-128">System.String</span></span>

## <span data-ttu-id="9d179-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d179-129">OUTPUTS</span></span>

### <span data-ttu-id="9d179-130">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="9d179-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="9d179-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d179-131">NOTES</span></span>

## <span data-ttu-id="9d179-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d179-132">RELATED LINKS</span></span>

[<span data-ttu-id="9d179-133">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9d179-133">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)



[<span data-ttu-id="9d179-134">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9d179-134">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9d179-135">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="9d179-135">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="9d179-136">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="9d179-136">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
