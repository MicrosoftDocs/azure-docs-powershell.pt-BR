---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 596B8A6F-D3C2-4170-BCD7-B7A1CDB656D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee767e1ba4c5008837e7cef98aafa4017465829
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946073"
---
# <span data-ttu-id="cbadd-101">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="cbadd-101">Restart-AzureVM</span></span>

## <span data-ttu-id="cbadd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbadd-102">SYNOPSIS</span></span>
<span data-ttu-id="cbadd-103">Reinicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbadd-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="cbadd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbadd-104">SYNTAX</span></span>

### <span data-ttu-id="cbadd-105">RestartByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="cbadd-105">RestartByName (Default)</span></span>
```
Restart-AzureVM [-Name] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cbadd-106">RedeployByName</span><span class="sxs-lookup"><span data-stu-id="cbadd-106">RedeployByName</span></span>
```
Restart-AzureVM [-Name] <String> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cbadd-107">InitiateMaintenanceByName</span><span class="sxs-lookup"><span data-stu-id="cbadd-107">InitiateMaintenanceByName</span></span>
```
Restart-AzureVM [-Name] <String> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cbadd-108">RestartInput</span><span class="sxs-lookup"><span data-stu-id="cbadd-108">RestartInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cbadd-109">RedeployInput</span><span class="sxs-lookup"><span data-stu-id="cbadd-109">RedeployInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cbadd-110">InitiateMaintenanceInput</span><span class="sxs-lookup"><span data-stu-id="cbadd-110">InitiateMaintenanceInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cbadd-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbadd-111">DESCRIPTION</span></span>
<span data-ttu-id="cbadd-112">O cmdlet **Restart-AzureVM** solicita uma reinicialização de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbadd-112">The **Restart-AzureVM** cmdlet requests a restart of an Azure virtual machine.</span></span>

## <span data-ttu-id="cbadd-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbadd-113">EXAMPLES</span></span>

### <span data-ttu-id="cbadd-114">Exemplo 1: reiniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="cbadd-114">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureVM -ServiceName "MyService01" -Name "MyVM"
```

<span data-ttu-id="cbadd-115">Esse comando reinicia a máquina virtual VirtualMachine27 em execução no serviço do Azure chamado Service01.</span><span class="sxs-lookup"><span data-stu-id="cbadd-115">This command restarts the VirtualMachine27 virtual machine running in the Azure service named Service01.</span></span>

### <span data-ttu-id="cbadd-116">Exemplo 2: reiniciar uma máquina virtual usando um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="cbadd-116">Example 2: Restart a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MyService01" -Name "VirtualMachine27" | Restart-AzureVM
```

<span data-ttu-id="cbadd-117">Esse comando recupera o objeto da máquina virtual para a máquina virtual nomeada MyVM e, em seguida, o reinicia.</span><span class="sxs-lookup"><span data-stu-id="cbadd-117">This command retrieves the virtual machine object for the virtual machine named MyVM and then restarts it.</span></span>

## <span data-ttu-id="cbadd-118">OS</span><span class="sxs-lookup"><span data-stu-id="cbadd-118">PARAMETERS</span></span>

### <span data-ttu-id="cbadd-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="cbadd-119">-InformationAction</span></span>
<span data-ttu-id="cbadd-120">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="cbadd-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cbadd-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cbadd-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbadd-122">Contínuo</span><span class="sxs-lookup"><span data-stu-id="cbadd-122">Continue</span></span>
- <span data-ttu-id="cbadd-123">Ignorar</span><span class="sxs-lookup"><span data-stu-id="cbadd-123">Ignore</span></span>
- <span data-ttu-id="cbadd-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="cbadd-124">Inquire</span></span>
- <span data-ttu-id="cbadd-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cbadd-125">SilentlyContinue</span></span>
- <span data-ttu-id="cbadd-126">Finaliza</span><span class="sxs-lookup"><span data-stu-id="cbadd-126">Stop</span></span>
- <span data-ttu-id="cbadd-127">Suspensão</span><span class="sxs-lookup"><span data-stu-id="cbadd-127">Suspend</span></span>

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

### <span data-ttu-id="cbadd-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cbadd-128">-InformationVariable</span></span>
<span data-ttu-id="cbadd-129">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="cbadd-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cbadd-130">-InitiateMaintenance</span><span class="sxs-lookup"><span data-stu-id="cbadd-130">-InitiateMaintenance</span></span>
<span data-ttu-id="cbadd-131">Iniciar a manutenção na máquina virtual</span><span class="sxs-lookup"><span data-stu-id="cbadd-131">Initiate Maintenance on the Virtual Machine</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: InitiateMaintenanceByName, InitiateMaintenanceInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadd-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="cbadd-132">-Name</span></span>
<span data-ttu-id="cbadd-133">Especifica o nome da máquina virtual a ser reiniciada.</span><span class="sxs-lookup"><span data-stu-id="cbadd-133">Specifies the name of the virtual machine to restart.</span></span>

```yaml
Type: String
Parameter Sets: RestartByName, RedeployByName, InitiateMaintenanceByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbadd-134">-Perfil</span><span class="sxs-lookup"><span data-stu-id="cbadd-134">-Profile</span></span>
<span data-ttu-id="cbadd-135">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="cbadd-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cbadd-136">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="cbadd-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cbadd-137">-Reimplantar</span><span class="sxs-lookup"><span data-stu-id="cbadd-137">-Redeploy</span></span>
<span data-ttu-id="cbadd-138">Indica que o cmdlet reimplanta a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cbadd-138">Indicates that the cmdlet redeploys the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployByName, RedeployInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadd-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cbadd-139">-ServiceName</span></span>
<span data-ttu-id="cbadd-140">Especifica o nome do serviço do Azure que contém a máquina virtual a ser reiniciada.</span><span class="sxs-lookup"><span data-stu-id="cbadd-140">Specifies the name of the Azure service that contains the virtual machine to restart.</span></span>

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

### <span data-ttu-id="cbadd-141">-VM</span><span class="sxs-lookup"><span data-stu-id="cbadd-141">-VM</span></span>
<span data-ttu-id="cbadd-142">Especifica um objeto de máquina virtual que identifica a máquina virtual para reiniciar.</span><span class="sxs-lookup"><span data-stu-id="cbadd-142">Specifies a virtual machine object that identifies the virtual machine to restart.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: RestartInput, RedeployInput, InitiateMaintenanceInput
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbadd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbadd-143">CommonParameters</span></span>
<span data-ttu-id="cbadd-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbadd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbadd-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbadd-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbadd-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbadd-146">INPUTS</span></span>

## <span data-ttu-id="cbadd-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbadd-147">OUTPUTS</span></span>

## <span data-ttu-id="cbadd-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbadd-148">NOTES</span></span>

## <span data-ttu-id="cbadd-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbadd-149">RELATED LINKS</span></span>

[<span data-ttu-id="cbadd-150">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="cbadd-150">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="cbadd-151">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="cbadd-151">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="cbadd-152">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="cbadd-152">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="cbadd-153">Parar-AzureVM</span><span class="sxs-lookup"><span data-stu-id="cbadd-153">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="cbadd-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="cbadd-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


