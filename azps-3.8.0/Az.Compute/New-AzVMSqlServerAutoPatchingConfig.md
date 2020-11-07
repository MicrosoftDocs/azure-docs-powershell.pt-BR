---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777587"
---
# <span data-ttu-id="7f201-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="7f201-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="7f201-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f201-102">SYNOPSIS</span></span>
<span data-ttu-id="7f201-103">Cria um objeto de configuração para a aplicação de patch automática em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7f201-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="7f201-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f201-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="7f201-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f201-105">DESCRIPTION</span></span>
<span data-ttu-id="7f201-106">O cmdlet **New-AzVMSqlServerAutoPatchingConfig** cria um objeto de configuração para a aplicação de patch automática em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7f201-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="7f201-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f201-107">EXAMPLES</span></span>

### <span data-ttu-id="7f201-108">Exemplo 1: criar um objeto de configuração para configurar a aplicação de patch automática</span><span class="sxs-lookup"><span data-stu-id="7f201-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="7f201-109">Esse comando cria o objeto de configuração para a aplicação de patch.</span><span class="sxs-lookup"><span data-stu-id="7f201-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="7f201-110">O comando especifica o dia da semana e define a janela de manutenção.</span><span class="sxs-lookup"><span data-stu-id="7f201-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="7f201-111">Essa configuração permite o patching que usa esses valores.</span><span class="sxs-lookup"><span data-stu-id="7f201-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="7f201-112">O comando armazena o resultado na variável $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="7f201-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="7f201-113">Você pode especificar esse item de configuração para outros cmdlets, como o cmdlet Set-AzVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="7f201-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="7f201-114">OS</span><span class="sxs-lookup"><span data-stu-id="7f201-114">PARAMETERS</span></span>

### <span data-ttu-id="7f201-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="7f201-115">-DayOfWeek</span></span>
<span data-ttu-id="7f201-116">Especifica o dia da semana em que as atualizações devem ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="7f201-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="7f201-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7f201-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f201-118">Domingo</span><span class="sxs-lookup"><span data-stu-id="7f201-118">Sunday</span></span>
- <span data-ttu-id="7f201-119">Sexta</span><span class="sxs-lookup"><span data-stu-id="7f201-119">Monday</span></span>
- <span data-ttu-id="7f201-120">-</span><span class="sxs-lookup"><span data-stu-id="7f201-120">Tuesday</span></span>
- <span data-ttu-id="7f201-121">Feira</span><span class="sxs-lookup"><span data-stu-id="7f201-121">Wednesday</span></span>
- <span data-ttu-id="7f201-122">Terça</span><span class="sxs-lookup"><span data-stu-id="7f201-122">Thursday</span></span>
- <span data-ttu-id="7f201-123">Às</span><span class="sxs-lookup"><span data-stu-id="7f201-123">Friday</span></span>
- <span data-ttu-id="7f201-124">Sábado</span><span class="sxs-lookup"><span data-stu-id="7f201-124">Saturday</span></span>
- <span data-ttu-id="7f201-125">Diário</span><span class="sxs-lookup"><span data-stu-id="7f201-125">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f201-126">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="7f201-126">-Enable</span></span>
<span data-ttu-id="7f201-127">Indica que a aplicação de patch automatizada para a máquina virtual está habilitada.</span><span class="sxs-lookup"><span data-stu-id="7f201-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="7f201-128">Se você habilitar a aplicação de patch automatizada, o cmdlet colocará o Windows Update no modo interativo.</span><span class="sxs-lookup"><span data-stu-id="7f201-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="7f201-129">Se você desabilitar a aplicação de patch automatizada, as configurações do Windows Update não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="7f201-129">If you disable automated patching, Windows Update settings do not change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f201-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="7f201-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="7f201-131">Especifica a duração, em minutos, da janela de manutenção.</span><span class="sxs-lookup"><span data-stu-id="7f201-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="7f201-132">A aplicação de patch automatizada evita executar uma ação que pode afetar uma disponibilidade da máquina virtual fora da janela.</span><span class="sxs-lookup"><span data-stu-id="7f201-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="7f201-133">Especifique um múltiplo de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="7f201-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f201-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="7f201-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="7f201-135">Especifica a hora do dia em que a janela de manutenção é iniciada.</span><span class="sxs-lookup"><span data-stu-id="7f201-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="7f201-136">Esse tempo define quando as atualizações começam a ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="7f201-136">This time defines when updates start to install.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f201-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="7f201-137">-PatchCategory</span></span>
<span data-ttu-id="7f201-138">Especifica se atualizações importantes devem ser incluídas.</span><span class="sxs-lookup"><span data-stu-id="7f201-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f201-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f201-139">CommonParameters</span></span>
<span data-ttu-id="7f201-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f201-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f201-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f201-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f201-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f201-142">INPUTS</span></span>

### <span data-ttu-id="7f201-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7f201-143">None</span></span>

## <span data-ttu-id="7f201-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f201-144">OUTPUTS</span></span>

### <span data-ttu-id="7f201-145">Microsoft. Azure. Commands. COMPUTE. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="7f201-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="7f201-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f201-146">NOTES</span></span>

## <span data-ttu-id="7f201-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f201-147">RELATED LINKS</span></span>

[<span data-ttu-id="7f201-148">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="7f201-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="7f201-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7f201-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


