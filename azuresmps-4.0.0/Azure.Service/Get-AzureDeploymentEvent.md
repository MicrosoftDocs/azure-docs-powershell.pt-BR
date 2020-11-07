---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6715B3E8-6880-4B86-B831-41664766E12B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 026e06a0071084f07ed0b609b8b686e6cba44cc5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945650"
---
# <span data-ttu-id="b652a-101">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="b652a-101">Get-AzureDeploymentEvent</span></span>

## <span data-ttu-id="b652a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b652a-102">SYNOPSIS</span></span>
<span data-ttu-id="b652a-103">Obtém informações sobre os eventos que o Azure inicia e afetam máquinas virtuais e serviços de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b652a-103">Gets information about events that Azure initiates that impact virtual machines and cloud services.</span></span>

## <span data-ttu-id="b652a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b652a-104">SYNTAX</span></span>

### <span data-ttu-id="b652a-105">GetDeploymentEventBySlot (padrão)</span><span class="sxs-lookup"><span data-stu-id="b652a-105">GetDeploymentEventBySlot (Default)</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b652a-106">GetDeploymentEventByName</span><span class="sxs-lookup"><span data-stu-id="b652a-106">GetDeploymentEventByName</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [-DeploymentName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b652a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b652a-107">DESCRIPTION</span></span>
<span data-ttu-id="b652a-108">O cmdlet **Get-AzureDeploymentEvent** Obtém informações sobre os eventos que o Azure inicia que afetam máquinas virtuais e serviços de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b652a-108">The **Get-AzureDeploymentEvent** cmdlet gets information regarding events that Azure initiates that impact virtual machines and cloud services.</span></span>
<span data-ttu-id="b652a-109">Esses eventos incluem eventos de manutenção planejados.</span><span class="sxs-lookup"><span data-stu-id="b652a-109">These events include planned maintenance events.</span></span>
<span data-ttu-id="b652a-110">Esse cmdlet retorna uma lista de eventos que identificam a instância de função ou máquina virtual afetada, o motivo do impacto e a hora de início do evento.</span><span class="sxs-lookup"><span data-stu-id="b652a-110">This cmdlet returns a list of events that identify the role instance or virtual machine impacted, the reason for the impact, and the start time of the event.</span></span>

## <span data-ttu-id="b652a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b652a-111">EXAMPLES</span></span>

### <span data-ttu-id="b652a-112">1:</span><span class="sxs-lookup"><span data-stu-id="b652a-112">1:</span></span>
```
Get-AzureDeploymentEvent -DeploymentName "ConstosoDeployment" -ServiceName "ContosoService"
```

## <span data-ttu-id="b652a-113">OS</span><span class="sxs-lookup"><span data-stu-id="b652a-113">PARAMETERS</span></span>

### <span data-ttu-id="b652a-114">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="b652a-114">-DeploymentName</span></span>
<span data-ttu-id="b652a-115">Especifica o nome da implantação para a qual esse cmdlet obtém eventos.</span><span class="sxs-lookup"><span data-stu-id="b652a-115">Specifies the name of the deployment for which this cmdlet gets events.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b652a-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b652a-116">-EndTime</span></span>
<span data-ttu-id="b652a-117">Especifica a hora de término dos eventos programados que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b652a-117">Specifies the ending time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b652a-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b652a-118">-InformationAction</span></span>
<span data-ttu-id="b652a-119">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="b652a-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b652a-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b652a-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b652a-121">Contínuo</span><span class="sxs-lookup"><span data-stu-id="b652a-121">Continue</span></span>
- <span data-ttu-id="b652a-122">Ignorar</span><span class="sxs-lookup"><span data-stu-id="b652a-122">Ignore</span></span>
- <span data-ttu-id="b652a-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="b652a-123">Inquire</span></span>
- <span data-ttu-id="b652a-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b652a-124">SilentlyContinue</span></span>
- <span data-ttu-id="b652a-125">Finaliza</span><span class="sxs-lookup"><span data-stu-id="b652a-125">Stop</span></span>
- <span data-ttu-id="b652a-126">Suspensão</span><span class="sxs-lookup"><span data-stu-id="b652a-126">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b652a-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b652a-127">-InformationVariable</span></span>
<span data-ttu-id="b652a-128">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="b652a-128">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b652a-129">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b652a-129">-Profile</span></span>
<span data-ttu-id="b652a-130">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b652a-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b652a-131">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b652a-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b652a-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b652a-132">-ServiceName</span></span>
<span data-ttu-id="b652a-133">Especifica o nome do serviço hospedado para o qual este cmdlet obtém eventos agendados.</span><span class="sxs-lookup"><span data-stu-id="b652a-133">Specifies the name of the hosted service for which this cmdlet gets scheduled events.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b652a-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="b652a-134">-Slot</span></span>
<span data-ttu-id="b652a-135">Especifica o ambiente da implantação para o qual esse cmdlet obtém eventos agendados.</span><span class="sxs-lookup"><span data-stu-id="b652a-135">Specifies the environment of the deployment for which this cmdlet gets scheduled events.</span></span>
<span data-ttu-id="b652a-136">Os valores válidos são: preparação e produção.</span><span class="sxs-lookup"><span data-stu-id="b652a-136">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="b652a-137">O valor padrão é produção.</span><span class="sxs-lookup"><span data-stu-id="b652a-137">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventBySlot
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b652a-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b652a-138">-StartTime</span></span>
<span data-ttu-id="b652a-139">Especifica a hora de início dos eventos programados que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b652a-139">Specifies the starting time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b652a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b652a-140">CommonParameters</span></span>
<span data-ttu-id="b652a-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b652a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b652a-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b652a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b652a-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b652a-143">INPUTS</span></span>

## <span data-ttu-id="b652a-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b652a-144">OUTPUTS</span></span>

## <span data-ttu-id="b652a-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b652a-145">NOTES</span></span>

## <span data-ttu-id="b652a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b652a-146">RELATED LINKS</span></span>

[<span data-ttu-id="b652a-147">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b652a-147">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)


