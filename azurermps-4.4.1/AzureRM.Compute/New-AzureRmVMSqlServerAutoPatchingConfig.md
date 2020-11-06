---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 17d99840bffb9063ad61dec00d4b7d5983118399
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441163"
---
# <span data-ttu-id="aadf6-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="aadf6-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="aadf6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aadf6-102">SYNOPSIS</span></span>
<span data-ttu-id="aadf6-103">Cria um objeto de configuração para a aplicação de patch automática em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aadf6-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aadf6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aadf6-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aadf6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aadf6-105">DESCRIPTION</span></span>
<span data-ttu-id="aadf6-106">O cmdlet **New-AzureVMSqlServerAutoPatchingConfig** cria um objeto de configuração para a aplicação de patch automática em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aadf6-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="aadf6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aadf6-107">EXAMPLES</span></span>

### <span data-ttu-id="aadf6-108">Exemplo 1: criar um objeto de configuração para configurar a aplicação de patch automática</span><span class="sxs-lookup"><span data-stu-id="aadf6-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="aadf6-109">Esse comando cria o objeto de configuração para a aplicação de patch.</span><span class="sxs-lookup"><span data-stu-id="aadf6-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="aadf6-110">O comando especifica o dia da semana e define a janela de manutenção.</span><span class="sxs-lookup"><span data-stu-id="aadf6-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="aadf6-111">Essa configuração permite o patching que usa esses valores.</span><span class="sxs-lookup"><span data-stu-id="aadf6-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="aadf6-112">O comando armazena o resultado na variável $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="aadf6-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="aadf6-113">Você pode especificar esse item de configuração para outros cmdlets, como o cmdlet Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="aadf6-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="aadf6-114">OS</span><span class="sxs-lookup"><span data-stu-id="aadf6-114">PARAMETERS</span></span>

### <span data-ttu-id="aadf6-115">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="aadf6-115">-Enable</span></span>
<span data-ttu-id="aadf6-116">Indica que a aplicação de patch automatizada para a máquina virtual está habilitada.</span><span class="sxs-lookup"><span data-stu-id="aadf6-116">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="aadf6-117">Se você habilitar a aplicação de patch automatizada, o cmdlet colocará o Windows Update no modo interativo.</span><span class="sxs-lookup"><span data-stu-id="aadf6-117">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="aadf6-118">Se você desabilitar a aplicação de patch automatizada, as configurações do Windows Update não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="aadf6-118">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="aadf6-119">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="aadf6-119">-DayOfWeek</span></span>
<span data-ttu-id="aadf6-120">Especifica o dia da semana em que as atualizações devem ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="aadf6-120">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="aadf6-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="aadf6-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aadf6-122">Domingo</span><span class="sxs-lookup"><span data-stu-id="aadf6-122">Sunday</span></span>
- <span data-ttu-id="aadf6-123">Sexta</span><span class="sxs-lookup"><span data-stu-id="aadf6-123">Monday</span></span>
- <span data-ttu-id="aadf6-124">-</span><span class="sxs-lookup"><span data-stu-id="aadf6-124">Tuesday</span></span>
- <span data-ttu-id="aadf6-125">Feira</span><span class="sxs-lookup"><span data-stu-id="aadf6-125">Wednesday</span></span>
- <span data-ttu-id="aadf6-126">Terça</span><span class="sxs-lookup"><span data-stu-id="aadf6-126">Thursday</span></span>
- <span data-ttu-id="aadf6-127">Às</span><span class="sxs-lookup"><span data-stu-id="aadf6-127">Friday</span></span>
- <span data-ttu-id="aadf6-128">Sábado</span><span class="sxs-lookup"><span data-stu-id="aadf6-128">Saturday</span></span>
- <span data-ttu-id="aadf6-129">Diário</span><span class="sxs-lookup"><span data-stu-id="aadf6-129">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aadf6-130">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="aadf6-130">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="aadf6-131">Especifica a hora do dia em que a janela de manutenção é iniciada.</span><span class="sxs-lookup"><span data-stu-id="aadf6-131">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="aadf6-132">Esse tempo define quando as atualizações começam a ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="aadf6-132">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="aadf6-133">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="aadf6-133">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="aadf6-134">Especifica a duração, em minutos, da janela de manutenção.</span><span class="sxs-lookup"><span data-stu-id="aadf6-134">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="aadf6-135">A aplicação de patch automatizada evita executar uma ação que pode afetar uma disponibilidade da máquina virtual fora da janela.</span><span class="sxs-lookup"><span data-stu-id="aadf6-135">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="aadf6-136">Especifique um múltiplo de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="aadf6-136">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="aadf6-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="aadf6-137">-PatchCategory</span></span>
<span data-ttu-id="aadf6-138">Especifica se atualizações importantes devem ser incluídas.</span><span class="sxs-lookup"><span data-stu-id="aadf6-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aadf6-139">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="aadf6-139">-InformationAction</span></span>
<span data-ttu-id="aadf6-140">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="aadf6-140">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aadf6-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aadf6-141">-InformationVariable</span></span>
<span data-ttu-id="aadf6-142">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="aadf6-142">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aadf6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aadf6-143">CommonParameters</span></span>
<span data-ttu-id="aadf6-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aadf6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aadf6-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aadf6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aadf6-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aadf6-146">INPUTS</span></span>

## <span data-ttu-id="aadf6-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aadf6-147">OUTPUTS</span></span>

### <span data-ttu-id="aadf6-148">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="aadf6-148">AutoPatchingSettings</span></span>
<span data-ttu-id="aadf6-149">Este cmdlet retorna um objeto que contém as configurações de correção automática.</span><span class="sxs-lookup"><span data-stu-id="aadf6-149">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="aadf6-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aadf6-150">NOTES</span></span>

## <span data-ttu-id="aadf6-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aadf6-151">RELATED LINKS</span></span>

[<span data-ttu-id="aadf6-152">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="aadf6-152">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="aadf6-153">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="aadf6-153">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


