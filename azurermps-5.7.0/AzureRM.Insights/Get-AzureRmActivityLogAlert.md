---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: 41ed224333d9d0ab1aa542629f46fcf6d8db5fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440856"
---
# <span data-ttu-id="6dead-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6dead-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="6dead-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6dead-102">SYNOPSIS</span></span>
<span data-ttu-id="6dead-103">Obtém um ou mais recursos de alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="6dead-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dead-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6dead-104">SYNTAX</span></span>

### <span data-ttu-id="6dead-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6dead-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dead-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6dead-106">GetByResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6dead-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6dead-107">DESCRIPTION</span></span>
<span data-ttu-id="6dead-108">O cmdlet **Get-AzureRmActivityLogAlert** Obtém um ou mais recursos de alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="6dead-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="6dead-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6dead-109">EXAMPLES</span></span>

### <span data-ttu-id="6dead-110">Exemplo 1: obter alertas de log de atividades por ID de assinatura</span><span class="sxs-lookup"><span data-stu-id="6dead-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="6dead-111">Esse comando lista todos os alertas de log de atividades para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="6dead-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="6dead-112">Exemplo 2: obter alertas de log de atividade para o grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="6dead-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="6dead-113">Este comando lista os alertas de log de atividades para o grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="6dead-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="6dead-114">Exemplo 3: obter um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="6dead-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="6dead-115">Esse comando lista um alerta de registro de atividades (um único elemento com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="6dead-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="6dead-116">OS</span><span class="sxs-lookup"><span data-stu-id="6dead-116">PARAMETERS</span></span>

### <span data-ttu-id="6dead-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dead-117">-DefaultProfile</span></span>
<span data-ttu-id="6dead-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6dead-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dead-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6dead-119">-Name</span></span>
<span data-ttu-id="6dead-120">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="6dead-120">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dead-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dead-121">-ResourceGroupName</span></span>
<span data-ttu-id="6dead-122">O nome do grupo de recursos onde existe o recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="6dead-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="6dead-123">Se o nome não for nulo ou estiver vazio, esse parâmetro deverá conter uma cadeia de caracteres não vazia.</span><span class="sxs-lookup"><span data-stu-id="6dead-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dead-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dead-124">CommonParameters</span></span>
<span data-ttu-id="6dead-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dead-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dead-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dead-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dead-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6dead-127">INPUTS</span></span>

### <span data-ttu-id="6dead-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6dead-128">None</span></span>

## <span data-ttu-id="6dead-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6dead-129">OUTPUTS</span></span>

### <span data-ttu-id="6dead-130"><System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource]</span><span class="sxs-lookup"><span data-stu-id="6dead-130"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource]</span></span>

### <span data-ttu-id="6dead-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6dead-131">None</span></span>

## <span data-ttu-id="6dead-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6dead-132">NOTES</span></span>

## <span data-ttu-id="6dead-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6dead-133">RELATED LINKS</span></span>

[<span data-ttu-id="6dead-134">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6dead-134">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6dead-135">Update-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6dead-135">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6dead-136">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6dead-136">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6dead-137">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="6dead-137">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="6dead-138">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="6dead-138">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
