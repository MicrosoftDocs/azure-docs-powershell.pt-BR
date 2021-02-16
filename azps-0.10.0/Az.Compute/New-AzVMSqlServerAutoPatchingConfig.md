---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3ba7ab00076a3a0634a0d4394270fe4a83ec8ede
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398250"
---
# <span data-ttu-id="b08f1-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="b08f1-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="b08f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b08f1-102">SYNOPSIS</span></span>
<span data-ttu-id="b08f1-103">Cria um objeto de configuração para o patch automático em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b08f1-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="b08f1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b08f1-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b08f1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b08f1-105">DESCRIPTION</span></span>
<span data-ttu-id="b08f1-106">O cmdlet **New-AzVMSqlServerAutoPatchingConfig** cria um objeto de configuração para o patch automático em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b08f1-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="b08f1-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b08f1-107">EXAMPLES</span></span>

### <span data-ttu-id="b08f1-108">Exemplo 1: Criar um objeto de configuração para configurar o patch automático</span><span class="sxs-lookup"><span data-stu-id="b08f1-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="b08f1-109">Esse comando cria um objeto de configuração para patch.</span><span class="sxs-lookup"><span data-stu-id="b08f1-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="b08f1-110">O comando especifica o dia da semana e define a janela de manutenção.</span><span class="sxs-lookup"><span data-stu-id="b08f1-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="b08f1-111">Essa configuração habilita o patch que usa esses valores.</span><span class="sxs-lookup"><span data-stu-id="b08f1-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="b08f1-112">O comando armazena o resultado na variável $AutoBackupConfig dados.</span><span class="sxs-lookup"><span data-stu-id="b08f1-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="b08f1-113">Você pode especificar esse item de configuração para outros cmdlets, como o Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b08f1-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="b08f1-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b08f1-114">PARAMETERS</span></span>

### <span data-ttu-id="b08f1-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="b08f1-115">-DayOfWeek</span></span>
<span data-ttu-id="b08f1-116">Especifica o dia da semana em que as atualizações devem ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="b08f1-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="b08f1-117">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b08f1-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b08f1-118">Domingo</span><span class="sxs-lookup"><span data-stu-id="b08f1-118">Sunday</span></span>
- <span data-ttu-id="b08f1-119">Segunda-feira</span><span class="sxs-lookup"><span data-stu-id="b08f1-119">Monday</span></span>
- <span data-ttu-id="b08f1-120">Terça</span><span class="sxs-lookup"><span data-stu-id="b08f1-120">Tuesday</span></span>
- <span data-ttu-id="b08f1-121">Quarta</span><span class="sxs-lookup"><span data-stu-id="b08f1-121">Wednesday</span></span>
- <span data-ttu-id="b08f1-122">Quinta</span><span class="sxs-lookup"><span data-stu-id="b08f1-122">Thursday</span></span>
- <span data-ttu-id="b08f1-123">Sexta</span><span class="sxs-lookup"><span data-stu-id="b08f1-123">Friday</span></span>
- <span data-ttu-id="b08f1-124">Sábado</span><span class="sxs-lookup"><span data-stu-id="b08f1-124">Saturday</span></span>
- <span data-ttu-id="b08f1-125">Diária</span><span class="sxs-lookup"><span data-stu-id="b08f1-125">Everyday</span></span>

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

### <span data-ttu-id="b08f1-126">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="b08f1-126">-Enable</span></span>
<span data-ttu-id="b08f1-127">Indica que o patch automatizado para o computador virtual está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b08f1-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="b08f1-128">Se você habilitar o patch automático, o cmdlet colocará o Windows Update no modo interativo.</span><span class="sxs-lookup"><span data-stu-id="b08f1-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="b08f1-129">Se você desabilitar o patch automático, as configurações do Windows Update não mudarão.</span><span class="sxs-lookup"><span data-stu-id="b08f1-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="b08f1-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="b08f1-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="b08f1-131">Especifica a duração, em minutos, da janela de manutenção.</span><span class="sxs-lookup"><span data-stu-id="b08f1-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="b08f1-132">O patch automatizado evita a execução de uma ação que pode afetar a disponibilidade de uma máquina virtual fora dessa janela.</span><span class="sxs-lookup"><span data-stu-id="b08f1-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="b08f1-133">Especifique um múltiplo de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="b08f1-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="b08f1-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="b08f1-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="b08f1-135">Especifica a hora do dia em que a janela de manutenção é iniciada.</span><span class="sxs-lookup"><span data-stu-id="b08f1-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="b08f1-136">Esse horário define quando as atualizações começam a ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="b08f1-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="b08f1-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="b08f1-137">-PatchCategory</span></span>
<span data-ttu-id="b08f1-138">Especifica se atualizações importantes devem ser incluídas.</span><span class="sxs-lookup"><span data-stu-id="b08f1-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="b08f1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08f1-139">CommonParameters</span></span>
<span data-ttu-id="b08f1-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b08f1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08f1-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b08f1-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08f1-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="b08f1-142">INPUTS</span></span>

### <span data-ttu-id="b08f1-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b08f1-143">None</span></span>
<span data-ttu-id="b08f1-144">Este cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b08f1-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b08f1-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="b08f1-145">OUTPUTS</span></span>

### <span data-ttu-id="b08f1-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="b08f1-146">AutoPatchingSettings</span></span>
<span data-ttu-id="b08f1-147">Este objeto de retorno de cmdlet contém configurações para o patch automático.</span><span class="sxs-lookup"><span data-stu-id="b08f1-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="b08f1-148">Notas</span><span class="sxs-lookup"><span data-stu-id="b08f1-148">NOTES</span></span>

## <span data-ttu-id="b08f1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b08f1-149">RELATED LINKS</span></span>

[<span data-ttu-id="b08f1-150">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="b08f1-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="b08f1-151">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b08f1-151">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


