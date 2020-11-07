---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945651"
---
# <span data-ttu-id="a0fd0-101">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="a0fd0-101">Get-AzureDataDisk</span></span>

## <span data-ttu-id="a0fd0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="a0fd0-103">Obtém discos de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-103">Gets Azure data disks.</span></span>

## <span data-ttu-id="a0fd0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0fd0-104">SYNTAX</span></span>

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a0fd0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0fd0-105">DESCRIPTION</span></span>
<span data-ttu-id="a0fd0-106">O cmdlet **Get-AzureDataDisk** Obtém um objeto que representa os discos de dados em uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-106">The **Get-AzureDataDisk** cmdlet gets an object that represents the data disks on an Azure virtual machine.</span></span>
<span data-ttu-id="a0fd0-107">Para obter um objeto de disco de dados específico, especifique o número da unidade lógica (LUN) do disco.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-107">To get a specific data disk object, specify the logical unit number (LUN) of the disk.</span></span>

## <span data-ttu-id="a0fd0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0fd0-108">EXAMPLES</span></span>

### <span data-ttu-id="a0fd0-109">Exemplo 1: obter todos os discos de dados de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="a0fd0-109">Example 1: Get all data disks for a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

<span data-ttu-id="a0fd0-110">Esse comando obtém a máquina virtual chamada VirtualMachine07 no serviço chamado ContosoService usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="a0fd0-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="a0fd0-111">O comando passa a máquina virtual para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a0fd0-112">O cmdlet atual Obtém todos os discos de dados para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-112">The current cmdlet gets all the data disks for this virtual machine.</span></span>

### <span data-ttu-id="a0fd0-113">Exemplo 2: obter um disco de dados específico para um vituralvirtual machinevirtual</span><span class="sxs-lookup"><span data-stu-id="a0fd0-113">Example 2: Get a specific data disk for a vituralvirtual machinevirtual</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

<span data-ttu-id="a0fd0-114">Esse comando obtém a máquina virtual chamada VirtualMachine07 no serviço chamado ContosoService.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="a0fd0-115">O comando passa a máquina virtual para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="a0fd0-116">O cmdlet atual Obtém o disco de dados que tem o LUN 2.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-116">The current cmdlet gets the data disk that has the LUN 2.</span></span>

## <span data-ttu-id="a0fd0-117">OS</span><span class="sxs-lookup"><span data-stu-id="a0fd0-117">PARAMETERS</span></span>

### <span data-ttu-id="a0fd0-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a0fd0-118">-InformationAction</span></span>
<span data-ttu-id="a0fd0-119">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a0fd0-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a0fd0-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0fd0-121">Contínuo</span><span class="sxs-lookup"><span data-stu-id="a0fd0-121">Continue</span></span>
- <span data-ttu-id="a0fd0-122">Ignorar</span><span class="sxs-lookup"><span data-stu-id="a0fd0-122">Ignore</span></span>
- <span data-ttu-id="a0fd0-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="a0fd0-123">Inquire</span></span>
- <span data-ttu-id="a0fd0-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a0fd0-124">SilentlyContinue</span></span>
- <span data-ttu-id="a0fd0-125">Finaliza</span><span class="sxs-lookup"><span data-stu-id="a0fd0-125">Stop</span></span>
- <span data-ttu-id="a0fd0-126">Suspensão</span><span class="sxs-lookup"><span data-stu-id="a0fd0-126">Suspend</span></span>

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

### <span data-ttu-id="a0fd0-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a0fd0-127">-InformationVariable</span></span>
<span data-ttu-id="a0fd0-128">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a0fd0-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="a0fd0-129">-Lun</span></span>
<span data-ttu-id="a0fd0-130">Especifica o LUN para a unidade de dados na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-130">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="a0fd0-131">Os valores válidos são: de 0 a 15.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-131">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0fd0-132">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a0fd0-132">-Profile</span></span>
<span data-ttu-id="a0fd0-133">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a0fd0-134">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a0fd0-135">-VM</span><span class="sxs-lookup"><span data-stu-id="a0fd0-135">-VM</span></span>
<span data-ttu-id="a0fd0-136">Especifica o objeto da máquina virtual para o qual esse cmdlet obtém discos de dados.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-136">Specifies the virtual machine object for which this cmdlet gets data disks.</span></span>
<span data-ttu-id="a0fd0-137">Para obter um objeto de máquina virtual, use o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="a0fd0-137">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0fd0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0fd0-138">CommonParameters</span></span>
<span data-ttu-id="a0fd0-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0fd0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0fd0-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0fd0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0fd0-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0fd0-141">INPUTS</span></span>

## <span data-ttu-id="a0fd0-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0fd0-142">OUTPUTS</span></span>

## <span data-ttu-id="a0fd0-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0fd0-143">NOTES</span></span>

## <span data-ttu-id="a0fd0-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0fd0-144">RELATED LINKS</span></span>

[<span data-ttu-id="a0fd0-145">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="a0fd0-145">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="a0fd0-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a0fd0-146">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="a0fd0-147">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="a0fd0-147">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="a0fd0-148">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="a0fd0-148">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)


