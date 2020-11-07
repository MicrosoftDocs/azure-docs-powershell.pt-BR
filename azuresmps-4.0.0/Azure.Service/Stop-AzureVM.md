---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945741"
---
# <span data-ttu-id="670d8-101">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="670d8-101">Stop-AzureVM</span></span>

## <span data-ttu-id="670d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="670d8-102">SYNOPSIS</span></span>
<span data-ttu-id="670d8-103">Desliga uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="670d8-103">Shuts down an Azure virtual machine.</span></span>

## <span data-ttu-id="670d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="670d8-104">SYNTAX</span></span>

### <span data-ttu-id="670d8-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="670d8-105">ByName (Default)</span></span>
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="670d8-106">Contribuição</span><span class="sxs-lookup"><span data-stu-id="670d8-106">Input</span></span>
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="670d8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="670d8-107">DESCRIPTION</span></span>
<span data-ttu-id="670d8-108">O cmdlet **Stop-AzureVM** desliga uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="670d8-108">The **Stop-AzureVM** cmdlet shuts down a virtual machine.</span></span>

## <span data-ttu-id="670d8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="670d8-109">EXAMPLES</span></span>

### <span data-ttu-id="670d8-110">Exemplo 1: desligar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="670d8-110">Example 1: Shut down a virtual machine</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

<span data-ttu-id="670d8-111">Esse comando desliga uma máquina virtual que o serviço especificado contém.</span><span class="sxs-lookup"><span data-stu-id="670d8-111">This command shuts down a virtual machine that the specified service contains.</span></span>

### <span data-ttu-id="670d8-112">Exemplo 2: desligar uma máquina virtual usando um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="670d8-112">Example 2: Shut down a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

<span data-ttu-id="670d8-113">Esse comando desliga uma máquina virtual que o serviço especificado contém, usando o objeto da máquina virtual que **Get-AzureVM** retorna.</span><span class="sxs-lookup"><span data-stu-id="670d8-113">This command shuts down a virtual machine that the specified service contains, by using the virtual machine object that **Get-AzureVM** returns.</span></span>

### <span data-ttu-id="670d8-114">Exemplo 3: encerrar uma VM e manter a VM provisionada</span><span class="sxs-lookup"><span data-stu-id="670d8-114">Example 3: Shut down a VM and keep the VM provisioned</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

<span data-ttu-id="670d8-115">Esse comando desliga uma máquina virtual que o serviço especificado contém e o mantém provisionado.</span><span class="sxs-lookup"><span data-stu-id="670d8-115">This command shuts down a virtual machine that the specified service contains, and keeps it provisioned.</span></span>

### <span data-ttu-id="670d8-116">Exemplo 4: encerrar uma VM e permitir a desalocação da última VM na implantação</span><span class="sxs-lookup"><span data-stu-id="670d8-116">Example 4: Shut down a VM and allow deallocation of the last VM in the deployment</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

<span data-ttu-id="670d8-117">Esse comando desliga uma máquina virtual que o serviço especificado contém e permite a desalocação da última máquina virtual na implantação.</span><span class="sxs-lookup"><span data-stu-id="670d8-117">This command shuts down a virtual machine that the specified service contains and allows deallocation of the last virtual machine in the deployment.</span></span>

### <span data-ttu-id="670d8-118">Exemplo 5: desligar várias VMs</span><span class="sxs-lookup"><span data-stu-id="670d8-118">Example 5: Shut down multiple VMs</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

<span data-ttu-id="670d8-119">Esse comando desliga várias máquinas virtuais que o serviço especificado contém.</span><span class="sxs-lookup"><span data-stu-id="670d8-119">This command shuts down multiple virtual machines that the specified service contains.</span></span>

## <span data-ttu-id="670d8-120">OS</span><span class="sxs-lookup"><span data-stu-id="670d8-120">PARAMETERS</span></span>

### <span data-ttu-id="670d8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="670d8-121">-Force</span></span>
<span data-ttu-id="670d8-122">Especifica se a desalocação da última máquina virtual em uma implantação deve ser permitida.</span><span class="sxs-lookup"><span data-stu-id="670d8-122">Specifies whether to allow the deallocation of the last virtual machine in a deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670d8-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="670d8-123">-InformationAction</span></span>
<span data-ttu-id="670d8-124">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="670d8-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="670d8-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="670d8-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="670d8-126">Contínuo</span><span class="sxs-lookup"><span data-stu-id="670d8-126">Continue</span></span>
- <span data-ttu-id="670d8-127">Ignorar</span><span class="sxs-lookup"><span data-stu-id="670d8-127">Ignore</span></span>
- <span data-ttu-id="670d8-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="670d8-128">Inquire</span></span>
- <span data-ttu-id="670d8-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="670d8-129">SilentlyContinue</span></span>
- <span data-ttu-id="670d8-130">Finaliza</span><span class="sxs-lookup"><span data-stu-id="670d8-130">Stop</span></span>
- <span data-ttu-id="670d8-131">Suspensão</span><span class="sxs-lookup"><span data-stu-id="670d8-131">Suspend</span></span>

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

### <span data-ttu-id="670d8-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="670d8-132">-InformationVariable</span></span>
<span data-ttu-id="670d8-133">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="670d8-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="670d8-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="670d8-134">-Name</span></span>
<span data-ttu-id="670d8-135">Especifica o nome da máquina virtual a ser encerrada.</span><span class="sxs-lookup"><span data-stu-id="670d8-135">Specifies the name of the virtual machine to shut down.</span></span>

<span data-ttu-id="670d8-136">Use o caractere curinga para parar várias máquinas virtuais de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="670d8-136">Use the wildcard character to stop multiple virtual machines asynchronously.</span></span>
<span data-ttu-id="670d8-137">Com um caractere curinga, esse cmdlet chama a operação de funções de desligamento https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) , em vez da operação de função de desligamento https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx ( https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .</span><span class="sxs-lookup"><span data-stu-id="670d8-137">With a wildcard character, this cmdlet calls the Shutdown Roleshttps://msdn.microsoft.com/en-us/library/azure/dn469421.aspx operation (https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx), instead of the Shutdown Rolehttps://msdn.microsoft.com/en-us/library/azure/jj157195.aspx operation (https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx).</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670d8-138">-Perfil</span><span class="sxs-lookup"><span data-stu-id="670d8-138">-Profile</span></span>
<span data-ttu-id="670d8-139">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="670d8-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="670d8-140">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="670d8-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="670d8-141">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="670d8-141">-ServiceName</span></span>
<span data-ttu-id="670d8-142">Especifica o nome do serviço do Azure que contém a máquina virtual a ser encerrada.</span><span class="sxs-lookup"><span data-stu-id="670d8-142">Specifies the name of the Azure service that contains the virtual machine to shut down.</span></span>

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

### <span data-ttu-id="670d8-143">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="670d8-143">-StayProvisioned</span></span>
<span data-ttu-id="670d8-144">Especifica que esse cmdlet mantém a máquina virtual provisionada.</span><span class="sxs-lookup"><span data-stu-id="670d8-144">Specifies that this cmdlet keeps the virtual machine provisioned.</span></span>

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

### <span data-ttu-id="670d8-145">-VM</span><span class="sxs-lookup"><span data-stu-id="670d8-145">-VM</span></span>
<span data-ttu-id="670d8-146">Especifica um objeto de máquina virtual que identifica a máquina virtual para desligar.</span><span class="sxs-lookup"><span data-stu-id="670d8-146">Specifies a virtual machine object that identifies the virtual machine to shut down.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670d8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670d8-147">CommonParameters</span></span>
<span data-ttu-id="670d8-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="670d8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670d8-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="670d8-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670d8-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="670d8-150">INPUTS</span></span>

## <span data-ttu-id="670d8-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="670d8-151">OUTPUTS</span></span>

## <span data-ttu-id="670d8-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="670d8-152">NOTES</span></span>

## <span data-ttu-id="670d8-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="670d8-153">RELATED LINKS</span></span>

[<span data-ttu-id="670d8-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="670d8-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="670d8-155">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="670d8-155">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="670d8-156">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="670d8-156">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="670d8-157">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="670d8-157">Start-AzureVM</span></span>](./Start-AzureVM.md)


