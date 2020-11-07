---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945791"
---
# <span data-ttu-id="927ed-101">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="927ed-101">Set-AzureVMSize</span></span>

## <span data-ttu-id="927ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="927ed-102">SYNOPSIS</span></span>
<span data-ttu-id="927ed-103">Define o tamanho de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="927ed-103">Sets the size of an Azure virtual machine.</span></span>

## <span data-ttu-id="927ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="927ed-104">SYNTAX</span></span>

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="927ed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="927ed-105">DESCRIPTION</span></span>
<span data-ttu-id="927ed-106">O cmdlet **set-AzureVMSize** atualiza o tamanho de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="927ed-106">The **Set-AzureVMSize** cmdlet updates the size of a virtual machine.</span></span>
<span data-ttu-id="927ed-107">Ele tem dois parâmetros: *instanceize* , que é o novo tamanho da máquina virtual e *VM* , que é um objeto de máquina virtual recuperado usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="927ed-107">It has two parameters: *InstanceSize* , which is the new size of the virtual machine, and *VM* , which is a virtual machine object retrieved by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="927ed-108">O resultado de **set-AzureVMSize** pode ser canalizado para o cmdlet **Update-AzureVM** ou armazenado em uma variável para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="927ed-108">The result of **Set-AzureVMSize** can be piped to the **Update-AzureVM** cmdlet or stored in a variable for later use.</span></span>
<span data-ttu-id="927ed-109">Nenhuma alteração real é feita até que **Update-AzureVM** seja executado.</span><span class="sxs-lookup"><span data-stu-id="927ed-109">No actual change is made until **Update-AzureVM** is executed.</span></span>

<span data-ttu-id="927ed-110">Observação: esse cmdlet exigirá que a máquina virtual seja reprovisionada e possa obter um novo endereço IP.</span><span class="sxs-lookup"><span data-stu-id="927ed-110">Note: This cmdlet will require the virtual machine to be re-provisioned and it might get a new IP address.</span></span>

## <span data-ttu-id="927ed-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="927ed-111">EXAMPLES</span></span>

### <span data-ttu-id="927ed-112">Exemplo 1: definir o tamanho de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="927ed-112">Example 1: Set the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

<span data-ttu-id="927ed-113">Este comando atualiza uma máquina virtual para dimensionar "pequeno".</span><span class="sxs-lookup"><span data-stu-id="927ed-113">This command updates a virtual machine to size "Small".</span></span>

## <span data-ttu-id="927ed-114">OS</span><span class="sxs-lookup"><span data-stu-id="927ed-114">PARAMETERS</span></span>

### <span data-ttu-id="927ed-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="927ed-115">-InformationAction</span></span>
<span data-ttu-id="927ed-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="927ed-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="927ed-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="927ed-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="927ed-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="927ed-118">Continue</span></span>
- <span data-ttu-id="927ed-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="927ed-119">Ignore</span></span>
- <span data-ttu-id="927ed-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="927ed-120">Inquire</span></span>
- <span data-ttu-id="927ed-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="927ed-121">SilentlyContinue</span></span>
- <span data-ttu-id="927ed-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="927ed-122">Stop</span></span>
- <span data-ttu-id="927ed-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="927ed-123">Suspend</span></span>

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

### <span data-ttu-id="927ed-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="927ed-124">-InformationVariable</span></span>
<span data-ttu-id="927ed-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="927ed-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="927ed-126">-Instanceize</span><span class="sxs-lookup"><span data-stu-id="927ed-126">-InstanceSize</span></span>
<span data-ttu-id="927ed-127">Especifica o tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="927ed-127">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="927ed-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="927ed-128">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="927ed-129">--ExtraSmall--pequeno--médio--grande--ExtraLarge--a5--a6--a7</span><span class="sxs-lookup"><span data-stu-id="927ed-129">--ExtraSmall --Small --Medium --Large --ExtraLarge --A5 --A6 --A7</span></span>

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

### <span data-ttu-id="927ed-130">-Perfil</span><span class="sxs-lookup"><span data-stu-id="927ed-130">-Profile</span></span>
<span data-ttu-id="927ed-131">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="927ed-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="927ed-132">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="927ed-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="927ed-133">-VM</span><span class="sxs-lookup"><span data-stu-id="927ed-133">-VM</span></span>
<span data-ttu-id="927ed-134">Especifica o objeto da máquina virtual persistente do qual esse cmdlet define o tamanho.</span><span class="sxs-lookup"><span data-stu-id="927ed-134">Specifies the persistent virtual machine object that this cmdlet sets the size of.</span></span>

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

### <span data-ttu-id="927ed-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="927ed-135">CommonParameters</span></span>
<span data-ttu-id="927ed-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="927ed-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="927ed-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="927ed-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="927ed-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="927ed-138">INPUTS</span></span>

## <span data-ttu-id="927ed-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="927ed-139">OUTPUTS</span></span>

## <span data-ttu-id="927ed-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="927ed-140">NOTES</span></span>

## <span data-ttu-id="927ed-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="927ed-141">RELATED LINKS</span></span>

[<span data-ttu-id="927ed-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="927ed-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="927ed-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="927ed-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


