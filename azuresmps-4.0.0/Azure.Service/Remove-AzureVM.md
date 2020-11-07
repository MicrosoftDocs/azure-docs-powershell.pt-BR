---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 455DB2C0-08A0-4D62-B8EE-7C3DB9AD8A8C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85040f07914aef02355f69baab093c75ce7e4afd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945516"
---
# <span data-ttu-id="a840e-101">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a840e-101">Remove-AzureVM</span></span>

## <span data-ttu-id="a840e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a840e-102">SYNOPSIS</span></span>
<span data-ttu-id="a840e-103">Remove uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="a840e-103">Removes an Azure virtual machine.</span></span>

## <span data-ttu-id="a840e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a840e-104">SYNTAX</span></span>

```
Remove-AzureVM [-Name] <String> [-DeleteVHD] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a840e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a840e-105">DESCRIPTION</span></span>
<span data-ttu-id="a840e-106">O cmdlet **Remove-AzureVM** exclui uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="a840e-106">The **Remove-AzureVM** cmdlet deletes an Azure virtual machine.</span></span>
<span data-ttu-id="a840e-107">Esse processo não exclui os arquivos. vhd subjacentes dos discos montados nessa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a840e-107">This process does not delete the underlying .vhd files of the disks mounted on that virtual machine.</span></span>

## <span data-ttu-id="a840e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a840e-108">EXAMPLES</span></span>

### <span data-ttu-id="a840e-109">Exemplo 1: remover uma máquina virtual de um serviço</span><span class="sxs-lookup"><span data-stu-id="a840e-109">Example 1: Remove a virtual machine from a service</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine03"
```

<span data-ttu-id="a840e-110">Esse comando Remove a máquina virtual nomeada VirtualMachine03 que é executada no serviço ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="a840e-110">This command removes the virtual machine named VirtualMachine03 that runs in the ContosoService03 service.</span></span>

### <span data-ttu-id="a840e-111">Exemplo 2: remover uma máquina virtual e excluir os arquivos. vhd</span><span class="sxs-lookup"><span data-stu-id="a840e-111">Example 2: Remove a virtual machine and delete the .vhd files</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" -DeleteVHD
```

<span data-ttu-id="a840e-112">Esse comando Remove a máquina virtual VirtualMachine04 que é executada no serviço ContosoService03 e especifica a remoção dos arquivos. VHD usando o parâmetro *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="a840e-112">This command removes the VirtualMachine04 virtual machine that runs in the ContosoService03 service, and specifies to remove the .vhd files using the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="a840e-113">OS</span><span class="sxs-lookup"><span data-stu-id="a840e-113">PARAMETERS</span></span>

### <span data-ttu-id="a840e-114">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="a840e-114">-DeleteVHD</span></span>
<span data-ttu-id="a840e-115">Especifica se esse cmdlet Remove a máquina virtual e os blobs de disco subjacentes.</span><span class="sxs-lookup"><span data-stu-id="a840e-115">Specifies whether this cmdlet removes the virtual machine and the underlying disk blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a840e-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a840e-116">-InformationAction</span></span>
<span data-ttu-id="a840e-117">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="a840e-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a840e-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a840e-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a840e-119">Contínuo</span><span class="sxs-lookup"><span data-stu-id="a840e-119">Continue</span></span>
- <span data-ttu-id="a840e-120">Ignorar</span><span class="sxs-lookup"><span data-stu-id="a840e-120">Ignore</span></span>
- <span data-ttu-id="a840e-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="a840e-121">Inquire</span></span>
- <span data-ttu-id="a840e-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a840e-122">SilentlyContinue</span></span>
- <span data-ttu-id="a840e-123">Finaliza</span><span class="sxs-lookup"><span data-stu-id="a840e-123">Stop</span></span>
- <span data-ttu-id="a840e-124">Suspensão</span><span class="sxs-lookup"><span data-stu-id="a840e-124">Suspend</span></span>

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

### <span data-ttu-id="a840e-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a840e-125">-InformationVariable</span></span>
<span data-ttu-id="a840e-126">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="a840e-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a840e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a840e-127">-Name</span></span>
<span data-ttu-id="a840e-128">Especifica o nome da máquina virtual que está sendo removida.</span><span class="sxs-lookup"><span data-stu-id="a840e-128">Specifies the name of the virtual machine being removed.</span></span>

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

### <span data-ttu-id="a840e-129">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a840e-129">-Profile</span></span>
<span data-ttu-id="a840e-130">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a840e-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a840e-131">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a840e-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a840e-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a840e-132">-ServiceName</span></span>
<span data-ttu-id="a840e-133">Especifica o nome do serviço do Azure do qual a máquina virtual está sendo removida.</span><span class="sxs-lookup"><span data-stu-id="a840e-133">Specifies the name of the Azure service from which the virtual machine is being removed.</span></span>

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

### <span data-ttu-id="a840e-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a840e-134">-Confirm</span></span>
<span data-ttu-id="a840e-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a840e-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a840e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a840e-136">-WhatIf</span></span>
<span data-ttu-id="a840e-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a840e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a840e-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a840e-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a840e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a840e-139">CommonParameters</span></span>
<span data-ttu-id="a840e-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a840e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a840e-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a840e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a840e-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a840e-142">INPUTS</span></span>

## <span data-ttu-id="a840e-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a840e-143">OUTPUTS</span></span>

## <span data-ttu-id="a840e-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a840e-144">NOTES</span></span>

## <span data-ttu-id="a840e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a840e-145">RELATED LINKS</span></span>

[<span data-ttu-id="a840e-146">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a840e-146">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="a840e-147">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="a840e-147">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="a840e-148">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a840e-148">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="a840e-149">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a840e-149">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="a840e-150">Parar-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a840e-150">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="a840e-151">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a840e-151">Update-AzureVM</span></span>](./Update-AzureVM.md)


