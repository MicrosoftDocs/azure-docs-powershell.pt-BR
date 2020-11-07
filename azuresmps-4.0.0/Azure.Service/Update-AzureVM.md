---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8DC10708-09CE-449C-BE20-1E9E49CCE08A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55d9879d6e6768bf3ad409c84a4fc1052d58d8b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946013"
---
# <span data-ttu-id="096cc-101">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="096cc-101">Update-AzureVM</span></span>

## <span data-ttu-id="096cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="096cc-102">SYNOPSIS</span></span>
<span data-ttu-id="096cc-103">Modifica a configuração de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="096cc-103">Modifies the configuration of an Azure virtual machine.</span></span>

## <span data-ttu-id="096cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="096cc-104">SYNTAX</span></span>

```
Update-AzureVM [-Name] <String> -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="096cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="096cc-105">DESCRIPTION</span></span>
<span data-ttu-id="096cc-106">O cmdlet **Update-AzureVM** aceita informações de atualização para a máquina virtual especificada e inicia a atualização.</span><span class="sxs-lookup"><span data-stu-id="096cc-106">The **Update-AzureVM** cmdlet accepts update information for the specified virtual machine and initiates the update.</span></span>
<span data-ttu-id="096cc-107">Você pode adicionar ou remover discos de dados, modificar o modo de cache de dados ou discos do sistema operacional, alterar os pontos de extremidade de rede ou alterar o tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="096cc-107">You can add or remove data disks, modify the cache mode of data or operating system disks, change the network endpoints, or change the size of the virtual machine.</span></span>

## <span data-ttu-id="096cc-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="096cc-108">EXAMPLES</span></span>

### <span data-ttu-id="096cc-109">Exemplo 1: atualizar o tamanho de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="096cc-109">Example 1: Update the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" | Set-AzureVMSize -InstanceSize "Medium" | Update-AzureVM
```

<span data-ttu-id="096cc-110">Esse comando altera o tamanho da máquina virtual nomeada VirtualMachine04, em execução no serviço chamado ContosoService03, para Medium.</span><span class="sxs-lookup"><span data-stu-id="096cc-110">This command changes the size of the virtual machine named VirtualMachine04, running in the service named ContosoService03, to Medium.</span></span>

### <span data-ttu-id="096cc-111">Exemplo 2: adicionar um disco de dados a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="096cc-111">Example 2: Add a data disk to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine05" | Add-AzureDataDisk -CreateNew -MediaLocation "https://ContosoStore1.blob.core.azure.com/vhds/Disk22.vhd" -DiskSizeInGB 128 -DiskLabel "Data-128" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="096cc-112">Esse comando adiciona um novo disco de dados à máquina virtual chamada VirtualMachine05, em execução no serviço chamado ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="096cc-112">This command adds a new data disk to the virtual machine named VirtualMachine05, running in the service named ContosoService03.</span></span>

## <span data-ttu-id="096cc-113">OS</span><span class="sxs-lookup"><span data-stu-id="096cc-113">PARAMETERS</span></span>

### <span data-ttu-id="096cc-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="096cc-114">-InformationAction</span></span>
<span data-ttu-id="096cc-115">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="096cc-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="096cc-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="096cc-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="096cc-117">Contínuo</span><span class="sxs-lookup"><span data-stu-id="096cc-117">Continue</span></span>
- <span data-ttu-id="096cc-118">Ignorar</span><span class="sxs-lookup"><span data-stu-id="096cc-118">Ignore</span></span>
- <span data-ttu-id="096cc-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="096cc-119">Inquire</span></span>
- <span data-ttu-id="096cc-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="096cc-120">SilentlyContinue</span></span>
- <span data-ttu-id="096cc-121">Finaliza</span><span class="sxs-lookup"><span data-stu-id="096cc-121">Stop</span></span>
- <span data-ttu-id="096cc-122">Suspensão</span><span class="sxs-lookup"><span data-stu-id="096cc-122">Suspend</span></span>

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

### <span data-ttu-id="096cc-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="096cc-123">-InformationVariable</span></span>
<span data-ttu-id="096cc-124">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="096cc-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="096cc-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="096cc-125">-Name</span></span>
<span data-ttu-id="096cc-126">Especifica o nome da máquina virtual a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="096cc-126">Specifies the name of the virtual machine to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="096cc-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="096cc-127">-Profile</span></span>
<span data-ttu-id="096cc-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="096cc-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="096cc-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="096cc-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="096cc-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="096cc-130">-ServiceName</span></span>
<span data-ttu-id="096cc-131">Especifica o nome do serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="096cc-131">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="096cc-132">-VM</span><span class="sxs-lookup"><span data-stu-id="096cc-132">-VM</span></span>
<span data-ttu-id="096cc-133">Especifica o objeto da máquina virtual que inclui configurações atualizadas.</span><span class="sxs-lookup"><span data-stu-id="096cc-133">Specifies the virtual machine object that includes updated settings.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="096cc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096cc-134">CommonParameters</span></span>
<span data-ttu-id="096cc-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="096cc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096cc-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="096cc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096cc-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="096cc-137">INPUTS</span></span>

## <span data-ttu-id="096cc-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="096cc-138">OUTPUTS</span></span>

## <span data-ttu-id="096cc-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="096cc-139">NOTES</span></span>

## <span data-ttu-id="096cc-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="096cc-140">RELATED LINKS</span></span>

[<span data-ttu-id="096cc-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="096cc-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="096cc-142">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="096cc-142">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="096cc-143">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="096cc-143">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="096cc-144">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="096cc-144">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="096cc-145">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="096cc-145">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="096cc-146">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="096cc-146">Set-AzureVMSize</span></span>](./Set-AzureVMSize.md)

[<span data-ttu-id="096cc-147">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="096cc-147">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="096cc-148">Parar-AzureVM</span><span class="sxs-lookup"><span data-stu-id="096cc-148">Stop-AzureVM</span></span>](./Stop-AzureVM.md)


