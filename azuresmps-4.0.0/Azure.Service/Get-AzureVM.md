---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946547"
---
# <span data-ttu-id="ecfe1-101">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ecfe1-101">Get-AzureVM</span></span>

## <span data-ttu-id="ecfe1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ecfe1-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfe1-103">Recupera informações de uma ou mais máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-103">Retrieves information from one or more Azure virtual machines.</span></span>

## <span data-ttu-id="ecfe1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecfe1-104">SYNTAX</span></span>

### <span data-ttu-id="ecfe1-105">ListAllVMs (padrão)</span><span class="sxs-lookup"><span data-stu-id="ecfe1-105">ListAllVMs (Default)</span></span>
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecfe1-106">GetVMByServiceAndVMName</span><span class="sxs-lookup"><span data-stu-id="ecfe1-106">GetVMByServiceAndVMName</span></span>
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ecfe1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ecfe1-107">DESCRIPTION</span></span>
<span data-ttu-id="ecfe1-108">O cmdlet **Get-AzureVM** recupera informações sobre máquinas virtuais executadas no Azure.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-108">The **Get-AzureVM** cmdlet retrieves information about virtual machines running in Azure.</span></span>
<span data-ttu-id="ecfe1-109">Ele retorna um objeto com informações em uma máquina virtual específica, ou se nenhuma máquina virtual for especificada, para todas as máquinas virtuais no serviço especificado da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-109">It returns an object with information on a specific virtual machine, or if no virtual machine is specified, for all the virtual machines in the specified service of the current subscription.</span></span>

## <span data-ttu-id="ecfe1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecfe1-110">EXAMPLES</span></span>

### <span data-ttu-id="ecfe1-111">Exemplo 1: recuperar informações em uma máquina virtual especificada</span><span class="sxs-lookup"><span data-stu-id="ecfe1-111">Example 1: Retrieve information on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

<span data-ttu-id="ecfe1-112">Esse comando retorna um objeto com informações sobre a máquina virtual do VirtualMachine02 em execução no serviço de nuvem do ContosoService01.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-112">This command returns an object with information on the VirtualMachine02 virtual machine running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="ecfe1-113">Exemplo 2: recuperar informações em todas as máquinas virtuais</span><span class="sxs-lookup"><span data-stu-id="ecfe1-113">Example 2: Retrieve information on all virtual machines</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

<span data-ttu-id="ecfe1-114">Esse comando recupera um objeto List com informações sobre todas as máquinas virtuais executadas no serviço de nuvem do ContosoService01.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-114">This command retrieves a list object with information on all of the virtual machines running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="ecfe1-115">Exemplo 3: exibir uma tabela de status da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="ecfe1-115">Example 3: Display a table of virtual machine statuses</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

<span data-ttu-id="ecfe1-116">Esse comando exibe uma tabela que mostra as máquinas virtuais em execução no serviço ContosoService01, o domínio de atualização e o status atual de cada máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-116">This command displays a table showing the virtual machines running on the ContosoService01 service, their Upgrade Domain, and the current status of each virtual machine.</span></span>

## <span data-ttu-id="ecfe1-117">OS</span><span class="sxs-lookup"><span data-stu-id="ecfe1-117">PARAMETERS</span></span>

### <span data-ttu-id="ecfe1-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ecfe1-118">-InformationAction</span></span>
<span data-ttu-id="ecfe1-119">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ecfe1-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ecfe1-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ecfe1-121">Contínuo</span><span class="sxs-lookup"><span data-stu-id="ecfe1-121">Continue</span></span>
- <span data-ttu-id="ecfe1-122">Ignorar</span><span class="sxs-lookup"><span data-stu-id="ecfe1-122">Ignore</span></span>
- <span data-ttu-id="ecfe1-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="ecfe1-123">Inquire</span></span>
- <span data-ttu-id="ecfe1-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ecfe1-124">SilentlyContinue</span></span>
- <span data-ttu-id="ecfe1-125">Finaliza</span><span class="sxs-lookup"><span data-stu-id="ecfe1-125">Stop</span></span>
- <span data-ttu-id="ecfe1-126">Suspensão</span><span class="sxs-lookup"><span data-stu-id="ecfe1-126">Suspend</span></span>

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

### <span data-ttu-id="ecfe1-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ecfe1-127">-InformationVariable</span></span>
<span data-ttu-id="ecfe1-128">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ecfe1-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecfe1-129">-Name</span></span>
<span data-ttu-id="ecfe1-130">Especifica o nome da máquina virtual para a qual recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-130">Specifies the name of the virtual machine for which to retrieve information.</span></span>
<span data-ttu-id="ecfe1-131">Se esse parâmetro não for fornecido, o cmdlet retornará um objeto List com informações sobre todas as máquinas virtuais no serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-131">If this parameter is not provided, the cmdlet returns a list object with information about all the virtual machines in the specified service.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfe1-132">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ecfe1-132">-Profile</span></span>
<span data-ttu-id="ecfe1-133">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ecfe1-134">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ecfe1-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ecfe1-135">-ServiceName</span></span>
<span data-ttu-id="ecfe1-136">Especifica o nome do serviço na nuvem para o qual você deve retornar informações da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-136">Specifies the name of the cloud service for which to return virtual machine information.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfe1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfe1-137">CommonParameters</span></span>
<span data-ttu-id="ecfe1-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfe1-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecfe1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfe1-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ecfe1-140">INPUTS</span></span>

## <span data-ttu-id="ecfe1-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ecfe1-141">OUTPUTS</span></span>

## <span data-ttu-id="ecfe1-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ecfe1-142">NOTES</span></span>

## <span data-ttu-id="ecfe1-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecfe1-143">RELATED LINKS</span></span>

[<span data-ttu-id="ecfe1-144">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ecfe1-144">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ecfe1-145">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="ecfe1-145">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="ecfe1-146">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ecfe1-146">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="ecfe1-147">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ecfe1-147">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="ecfe1-148">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ecfe1-148">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="ecfe1-149">Parar-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ecfe1-149">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="ecfe1-150">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ecfe1-150">Update-AzureVM</span></span>](./Update-AzureVM.md)


