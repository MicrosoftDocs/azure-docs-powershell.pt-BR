---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: b4a1204d25852aa75c7b68c90305aefe9cfefe6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441053"
---
# <span data-ttu-id="63f5f-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="63f5f-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="63f5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="63f5f-103">Obtém um ou mais recursos de alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="63f5f-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63f5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63f5f-104">SYNTAX</span></span>

### <span data-ttu-id="63f5f-105">Parâmetros padrão para obter um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="63f5f-105">Default parameters for get an activity log alert</span></span>
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63f5f-106">Parâmetros para garantir que o grupo de recursos seja fornecido quando o nome for fornecido</span><span class="sxs-lookup"><span data-stu-id="63f5f-106">Parameters to make sure the resource group is given when the name is given</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63f5f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63f5f-107">DESCRIPTION</span></span>
<span data-ttu-id="63f5f-108">O cmdlet **Get-AzureRmActivityLogAlert** Obtém um ou mais recursos de alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="63f5f-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="63f5f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63f5f-109">EXAMPLES</span></span>

### <span data-ttu-id="63f5f-110">Exemplo 1: obter alertas de log de atividades por ID de assinatura</span><span class="sxs-lookup"><span data-stu-id="63f5f-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="63f5f-111">Esse comando lista todos os alertas de log de atividades para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="63f5f-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="63f5f-112">Exemplo 2: obter alertas de log de atividade para o grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="63f5f-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="63f5f-113">Este comando lista os alertas de log de atividades para o grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="63f5f-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="63f5f-114">Exemplo 3: obter um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="63f5f-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="63f5f-115">Esse comando lista um alerta de registro de atividades (um único elemento com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="63f5f-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="63f5f-116">OS</span><span class="sxs-lookup"><span data-stu-id="63f5f-116">PARAMETERS</span></span>

### <span data-ttu-id="63f5f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="63f5f-117">-Name</span></span>
<span data-ttu-id="63f5f-118">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="63f5f-118">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63f5f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f5f-119">-ResourceGroupName</span></span>
<span data-ttu-id="63f5f-120">O nome do grupo de recursos onde existe o recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="63f5f-120">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="63f5f-121">Se o nome não for nulo ou estiver vazio, esse parâmetro deverá conter uma cadeia de caracteres não vazia.</span><span class="sxs-lookup"><span data-stu-id="63f5f-121">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to make sure the resource group is given when the name is given
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63f5f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f5f-122">-DefaultProfile</span></span>
<span data-ttu-id="63f5f-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63f5f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63f5f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f5f-124">CommonParameters</span></span>
<span data-ttu-id="63f5f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f5f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f5f-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f5f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f5f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63f5f-127">INPUTS</span></span>

### <span data-ttu-id="63f5f-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="63f5f-128">None</span></span>

## <span data-ttu-id="63f5f-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63f5f-129">OUTPUTS</span></span>

### <span data-ttu-id="63f5f-130"><System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource]</span><span class="sxs-lookup"><span data-stu-id="63f5f-130"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource]</span></span>

### <span data-ttu-id="63f5f-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="63f5f-131">None</span></span>

## <span data-ttu-id="63f5f-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63f5f-132">NOTES</span></span>

## <span data-ttu-id="63f5f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63f5f-133">RELATED LINKS</span></span>

[<span data-ttu-id="63f5f-134">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="63f5f-134">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="63f5f-135">Update-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="63f5f-135">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="63f5f-136">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="63f5f-136">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="63f5f-137">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="63f5f-137">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="63f5f-138">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="63f5f-138">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
