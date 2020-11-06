---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 516192dab6d075979a2d78cea72afaedb7a18231
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429872"
---
# <span data-ttu-id="e7f19-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="e7f19-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="e7f19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7f19-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f19-103">Cria um objeto de configuração para a aplicação de patch automática em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e7f19-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7f19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7f19-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="e7f19-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7f19-105">DESCRIPTION</span></span>
<span data-ttu-id="e7f19-106">O cmdlet **New-AzureVMSqlServerAutoPatchingConfig** cria um objeto de configuração para a aplicação de patch automática em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e7f19-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="e7f19-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7f19-107">EXAMPLES</span></span>

### <span data-ttu-id="e7f19-108">Exemplo 1: criar um objeto de configuração para configurar a aplicação de patch automática</span><span class="sxs-lookup"><span data-stu-id="e7f19-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="e7f19-109">Esse comando cria o objeto de configuração para a aplicação de patch.</span><span class="sxs-lookup"><span data-stu-id="e7f19-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="e7f19-110">O comando especifica o dia da semana e define a janela de manutenção.</span><span class="sxs-lookup"><span data-stu-id="e7f19-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="e7f19-111">Essa configuração permite o patching que usa esses valores.</span><span class="sxs-lookup"><span data-stu-id="e7f19-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="e7f19-112">O comando armazena o resultado na variável $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="e7f19-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="e7f19-113">Você pode especificar esse item de configuração para outros cmdlets, como o cmdlet Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="e7f19-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="e7f19-114">OS</span><span class="sxs-lookup"><span data-stu-id="e7f19-114">PARAMETERS</span></span>

### <span data-ttu-id="e7f19-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="e7f19-115">-DayOfWeek</span></span>
<span data-ttu-id="e7f19-116">Especifica o dia da semana em que as atualizações devem ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="e7f19-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="e7f19-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e7f19-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7f19-118">Domingo</span><span class="sxs-lookup"><span data-stu-id="e7f19-118">Sunday</span></span>
- <span data-ttu-id="e7f19-119">Sexta</span><span class="sxs-lookup"><span data-stu-id="e7f19-119">Monday</span></span>
- <span data-ttu-id="e7f19-120">-</span><span class="sxs-lookup"><span data-stu-id="e7f19-120">Tuesday</span></span>
- <span data-ttu-id="e7f19-121">Feira</span><span class="sxs-lookup"><span data-stu-id="e7f19-121">Wednesday</span></span>
- <span data-ttu-id="e7f19-122">Terça</span><span class="sxs-lookup"><span data-stu-id="e7f19-122">Thursday</span></span>
- <span data-ttu-id="e7f19-123">Às</span><span class="sxs-lookup"><span data-stu-id="e7f19-123">Friday</span></span>
- <span data-ttu-id="e7f19-124">Sábado</span><span class="sxs-lookup"><span data-stu-id="e7f19-124">Saturday</span></span>
- <span data-ttu-id="e7f19-125">Diário</span><span class="sxs-lookup"><span data-stu-id="e7f19-125">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f19-126">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="e7f19-126">-Enable</span></span>
<span data-ttu-id="e7f19-127">Indica que a aplicação de patch automatizada para a máquina virtual está habilitada.</span><span class="sxs-lookup"><span data-stu-id="e7f19-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="e7f19-128">Se você habilitar a aplicação de patch automatizada, o cmdlet colocará o Windows Update no modo interativo.</span><span class="sxs-lookup"><span data-stu-id="e7f19-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="e7f19-129">Se você desabilitar a aplicação de patch automatizada, as configurações do Windows Update não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="e7f19-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="e7f19-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="e7f19-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="e7f19-131">Especifica a duração, em minutos, da janela de manutenção.</span><span class="sxs-lookup"><span data-stu-id="e7f19-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="e7f19-132">A aplicação de patch automatizada evita executar uma ação que pode afetar uma disponibilidade da máquina virtual fora da janela.</span><span class="sxs-lookup"><span data-stu-id="e7f19-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="e7f19-133">Especifique um múltiplo de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="e7f19-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="e7f19-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="e7f19-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="e7f19-135">Especifica a hora do dia em que a janela de manutenção é iniciada.</span><span class="sxs-lookup"><span data-stu-id="e7f19-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="e7f19-136">Esse tempo define quando as atualizações começam a ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="e7f19-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="e7f19-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="e7f19-137">-PatchCategory</span></span>
<span data-ttu-id="e7f19-138">Especifica se atualizações importantes devem ser incluídas.</span><span class="sxs-lookup"><span data-stu-id="e7f19-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f19-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f19-139">CommonParameters</span></span>
<span data-ttu-id="e7f19-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f19-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f19-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f19-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f19-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7f19-142">INPUTS</span></span>

### <span data-ttu-id="e7f19-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e7f19-143">None</span></span>
<span data-ttu-id="e7f19-144">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e7f19-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e7f19-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7f19-145">OUTPUTS</span></span>

### <span data-ttu-id="e7f19-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="e7f19-146">AutoPatchingSettings</span></span>
<span data-ttu-id="e7f19-147">Este cmdlet retorna um objeto que contém as configurações de correção automática.</span><span class="sxs-lookup"><span data-stu-id="e7f19-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="e7f19-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7f19-148">NOTES</span></span>

## <span data-ttu-id="e7f19-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7f19-149">RELATED LINKS</span></span>

[<span data-ttu-id="e7f19-150">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="e7f19-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="e7f19-151">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e7f19-151">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


