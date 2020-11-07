---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948411"
---
# <span data-ttu-id="b19dd-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="b19dd-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="b19dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b19dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b19dd-103">Cria um objeto de configuração para a aplicação de patch automática em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b19dd-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="b19dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b19dd-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="b19dd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b19dd-105">DESCRIPTION</span></span>
<span data-ttu-id="b19dd-106">O cmdlet **New-AzVMSqlServerAutoPatchingConfig** cria um objeto de configuração para a aplicação de patch automática em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b19dd-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="b19dd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b19dd-107">EXAMPLES</span></span>

### <span data-ttu-id="b19dd-108">Exemplo 1: criar um objeto de configuração para configurar a aplicação de patch automática</span><span class="sxs-lookup"><span data-stu-id="b19dd-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="b19dd-109">Esse comando cria o objeto de configuração para a aplicação de patch.</span><span class="sxs-lookup"><span data-stu-id="b19dd-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="b19dd-110">O comando especifica o dia da semana e define a janela de manutenção.</span><span class="sxs-lookup"><span data-stu-id="b19dd-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="b19dd-111">Essa configuração permite o patching que usa esses valores.</span><span class="sxs-lookup"><span data-stu-id="b19dd-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="b19dd-112">O comando armazena o resultado na variável $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="b19dd-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="b19dd-113">Você pode especificar esse item de configuração para outros cmdlets, como o cmdlet Set-AzVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="b19dd-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="b19dd-114">OS</span><span class="sxs-lookup"><span data-stu-id="b19dd-114">PARAMETERS</span></span>

### <span data-ttu-id="b19dd-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="b19dd-115">-DayOfWeek</span></span>
<span data-ttu-id="b19dd-116">Especifica o dia da semana em que as atualizações devem ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="b19dd-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="b19dd-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b19dd-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b19dd-118">Domingo</span><span class="sxs-lookup"><span data-stu-id="b19dd-118">Sunday</span></span>
- <span data-ttu-id="b19dd-119">Sexta</span><span class="sxs-lookup"><span data-stu-id="b19dd-119">Monday</span></span>
- <span data-ttu-id="b19dd-120">-</span><span class="sxs-lookup"><span data-stu-id="b19dd-120">Tuesday</span></span>
- <span data-ttu-id="b19dd-121">Feira</span><span class="sxs-lookup"><span data-stu-id="b19dd-121">Wednesday</span></span>
- <span data-ttu-id="b19dd-122">Terça</span><span class="sxs-lookup"><span data-stu-id="b19dd-122">Thursday</span></span>
- <span data-ttu-id="b19dd-123">Às</span><span class="sxs-lookup"><span data-stu-id="b19dd-123">Friday</span></span>
- <span data-ttu-id="b19dd-124">Sábado</span><span class="sxs-lookup"><span data-stu-id="b19dd-124">Saturday</span></span>
- <span data-ttu-id="b19dd-125">Diário</span><span class="sxs-lookup"><span data-stu-id="b19dd-125">Everyday</span></span>

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

### <span data-ttu-id="b19dd-126">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="b19dd-126">-Enable</span></span>
<span data-ttu-id="b19dd-127">Indica que a aplicação de patch automatizada para a máquina virtual está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b19dd-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="b19dd-128">Se você habilitar a aplicação de patch automatizada, o cmdlet colocará o Windows Update no modo interativo.</span><span class="sxs-lookup"><span data-stu-id="b19dd-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="b19dd-129">Se você desabilitar a aplicação de patch automatizada, as configurações do Windows Update não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="b19dd-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="b19dd-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="b19dd-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="b19dd-131">Especifica a duração, em minutos, da janela de manutenção.</span><span class="sxs-lookup"><span data-stu-id="b19dd-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="b19dd-132">A aplicação de patch automatizada evita executar uma ação que pode afetar uma disponibilidade da máquina virtual fora da janela.</span><span class="sxs-lookup"><span data-stu-id="b19dd-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="b19dd-133">Especifique um múltiplo de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="b19dd-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="b19dd-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="b19dd-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="b19dd-135">Especifica a hora do dia em que a janela de manutenção é iniciada.</span><span class="sxs-lookup"><span data-stu-id="b19dd-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="b19dd-136">Esse tempo define quando as atualizações começam a ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="b19dd-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="b19dd-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="b19dd-137">-PatchCategory</span></span>
<span data-ttu-id="b19dd-138">Especifica se atualizações importantes devem ser incluídas.</span><span class="sxs-lookup"><span data-stu-id="b19dd-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="b19dd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b19dd-139">CommonParameters</span></span>
<span data-ttu-id="b19dd-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b19dd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b19dd-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b19dd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b19dd-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b19dd-142">INPUTS</span></span>

### <span data-ttu-id="b19dd-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b19dd-143">None</span></span>

## <span data-ttu-id="b19dd-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b19dd-144">OUTPUTS</span></span>

### <span data-ttu-id="b19dd-145">Microsoft. Azure. Commands. COMPUTE. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="b19dd-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="b19dd-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b19dd-146">NOTES</span></span>

## <span data-ttu-id="b19dd-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b19dd-147">RELATED LINKS</span></span>

[<span data-ttu-id="b19dd-148">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="b19dd-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="b19dd-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b19dd-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


