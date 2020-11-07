---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946191"
---
# <span data-ttu-id="59ebf-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="59ebf-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="59ebf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="59ebf-103">Cria um objeto de configuração para a aplicação de patch automática da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="59ebf-103">Creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="59ebf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59ebf-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="59ebf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59ebf-105">DESCRIPTION</span></span>
<span data-ttu-id="59ebf-106">O cmdlet **New-AzureVMSqlServerAutoPatchingConfig** cria um objeto de configuração para o patch automático da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="59ebf-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="59ebf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59ebf-107">EXAMPLES</span></span>

### <span data-ttu-id="59ebf-108">Exemplo 1: criar um objeto de configuração para configurar a aplicação de patch automática</span><span class="sxs-lookup"><span data-stu-id="59ebf-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

<span data-ttu-id="59ebf-109">Esse comando cria um objeto de configuração que pode ser usado para configurar a aplicação de patch automática usando Set-AzureVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="59ebf-109">This command creates configuration object that can be used to configure automatic patching using Set-AzureVMSqlServerExtension.</span></span>

## <span data-ttu-id="59ebf-110">OS</span><span class="sxs-lookup"><span data-stu-id="59ebf-110">PARAMETERS</span></span>

### <span data-ttu-id="59ebf-111">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="59ebf-111">-DayOfWeek</span></span>
<span data-ttu-id="59ebf-112">Especifica o dia da semana em que as atualizações devem ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="59ebf-112">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="59ebf-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="59ebf-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59ebf-114">Domingo</span><span class="sxs-lookup"><span data-stu-id="59ebf-114">Sunday</span></span>
- <span data-ttu-id="59ebf-115">Sexta</span><span class="sxs-lookup"><span data-stu-id="59ebf-115">Monday</span></span>
- <span data-ttu-id="59ebf-116">-</span><span class="sxs-lookup"><span data-stu-id="59ebf-116">Tuesday</span></span>
- <span data-ttu-id="59ebf-117">Feira</span><span class="sxs-lookup"><span data-stu-id="59ebf-117">Wednesday</span></span>
- <span data-ttu-id="59ebf-118">Terça</span><span class="sxs-lookup"><span data-stu-id="59ebf-118">Thursday</span></span>
- <span data-ttu-id="59ebf-119">Às</span><span class="sxs-lookup"><span data-stu-id="59ebf-119">Friday</span></span>
- <span data-ttu-id="59ebf-120">Sábado</span><span class="sxs-lookup"><span data-stu-id="59ebf-120">Saturday</span></span>
- <span data-ttu-id="59ebf-121">Diário</span><span class="sxs-lookup"><span data-stu-id="59ebf-121">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ebf-122">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="59ebf-122">-Enable</span></span>
<span data-ttu-id="59ebf-123">Indica que a aplicação de patch automatizada para a máquina virtual está habilitada.</span><span class="sxs-lookup"><span data-stu-id="59ebf-123">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="59ebf-124">Se você habilitar a aplicação de patch automatizada, o cmdlet colocará o Windows Update no modo interativo.</span><span class="sxs-lookup"><span data-stu-id="59ebf-124">If you enable automated patching the cmdlet will put Windows Update into interactive mode.</span></span>
<span data-ttu-id="59ebf-125">Se você desabilitar a aplicação de patch automatizada, as configurações do Windows Update não serão alteradas.</span><span class="sxs-lookup"><span data-stu-id="59ebf-125">If you disable automated patching, Windows Update settings will not change.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ebf-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="59ebf-126">-InformationAction</span></span>
<span data-ttu-id="59ebf-127">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="59ebf-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="59ebf-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="59ebf-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59ebf-129">Contínuo</span><span class="sxs-lookup"><span data-stu-id="59ebf-129">Continue</span></span>
- <span data-ttu-id="59ebf-130">Ignorar</span><span class="sxs-lookup"><span data-stu-id="59ebf-130">Ignore</span></span>
- <span data-ttu-id="59ebf-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="59ebf-131">Inquire</span></span>
- <span data-ttu-id="59ebf-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="59ebf-132">SilentlyContinue</span></span>
- <span data-ttu-id="59ebf-133">Finaliza</span><span class="sxs-lookup"><span data-stu-id="59ebf-133">Stop</span></span>
- <span data-ttu-id="59ebf-134">Suspensão</span><span class="sxs-lookup"><span data-stu-id="59ebf-134">Suspend</span></span>

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

### <span data-ttu-id="59ebf-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="59ebf-135">-InformationVariable</span></span>
<span data-ttu-id="59ebf-136">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="59ebf-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="59ebf-137">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="59ebf-137">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="59ebf-138">Especifica a duração da janela de manutenção.</span><span class="sxs-lookup"><span data-stu-id="59ebf-138">Specifies the duration of the maintenance window.</span></span>
<span data-ttu-id="59ebf-139">A aplicação de patch automatizada evitará executar uma ação que pode afetar a disponibilidade de uma máquina virtual fora da janela.</span><span class="sxs-lookup"><span data-stu-id="59ebf-139">Automated patching will avoid performing an action that can impact a virtual machine availability outside of that window.</span></span>
<span data-ttu-id="59ebf-140">Somente incrementos de 30 minutos são permitidos.</span><span class="sxs-lookup"><span data-stu-id="59ebf-140">Only 30 minutes increments are allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ebf-141">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="59ebf-141">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="59ebf-142">Especifica a hora do dia em que a janela de manutenção é iniciada.</span><span class="sxs-lookup"><span data-stu-id="59ebf-142">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="59ebf-143">Esse tempo define quando as atualizações iniciam a instalação e são arredondadas para a hora.</span><span class="sxs-lookup"><span data-stu-id="59ebf-143">This time defines when updates start installing and is rounded to the hour.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ebf-144">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="59ebf-144">-PatchCategory</span></span>
<span data-ttu-id="59ebf-145">Especifica se atualizações importantes devem ser incluídas.</span><span class="sxs-lookup"><span data-stu-id="59ebf-145">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ebf-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ebf-146">CommonParameters</span></span>
<span data-ttu-id="59ebf-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59ebf-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ebf-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59ebf-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ebf-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59ebf-149">INPUTS</span></span>

## <span data-ttu-id="59ebf-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59ebf-150">OUTPUTS</span></span>

### <span data-ttu-id="59ebf-151">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="59ebf-151">AutoPatchingSettings</span></span>
<span data-ttu-id="59ebf-152">Este cmdlet retorna um objeto que contém as configurações de correção automática.</span><span class="sxs-lookup"><span data-stu-id="59ebf-152">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="59ebf-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59ebf-153">NOTES</span></span>

## <span data-ttu-id="59ebf-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59ebf-154">RELATED LINKS</span></span>

[<span data-ttu-id="59ebf-155">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="59ebf-155">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)

[<span data-ttu-id="59ebf-156">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="59ebf-156">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="59ebf-157">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="59ebf-157">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


