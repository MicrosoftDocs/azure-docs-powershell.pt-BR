---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BEE9430-D6BF-49F1-A23D-32784C6C818E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 98b9abe6bcb9998067fe978a5f99f5d8b64cd26d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946331"
---
# <span data-ttu-id="f74c4-101">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="f74c4-101">Get-AzurePublicIP</span></span>

## <span data-ttu-id="f74c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f74c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f74c4-103">Obtém as informações de IP público para uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f74c4-103">Gets the Public IP information for an Azure virtual machine.</span></span>

## <span data-ttu-id="f74c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f74c4-104">SYNTAX</span></span>

```
Get-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f74c4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f74c4-105">DESCRIPTION</span></span>
<span data-ttu-id="f74c4-106">O cmdlet **Get-AzurePublicIP** Obtém as informações de IP público para uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f74c4-106">The **Get-AzurePublicIP** cmdlet gets the Public IP information for an Azure virtual machine.</span></span>
<span data-ttu-id="f74c4-107">Para obter o endereço IP do IP público, use o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="f74c4-107">To obtain the IP address of the Public IP, use the **Get-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="f74c4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f74c4-108">EXAMPLES</span></span>

### <span data-ttu-id="f74c4-109">Exemplo 1: obter configuração de IP público</span><span class="sxs-lookup"><span data-stu-id="f74c4-109">Example 1: Get Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Get-AzurePublicIP
```

<span data-ttu-id="f74c4-110">Esse comando obtém a máquina virtual chamada FTPInstance no serviço chamado FTPInAzure usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="f74c4-110">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="f74c4-111">O comando transmite a máquina virtual para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="f74c4-111">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f74c4-112">O cmdlet atual Obtém a configuração de IP público da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f74c4-112">The current cmdlet gets Public IP configuration from the virtual machine.</span></span>

## <span data-ttu-id="f74c4-113">OS</span><span class="sxs-lookup"><span data-stu-id="f74c4-113">PARAMETERS</span></span>

### <span data-ttu-id="f74c4-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f74c4-114">-InformationAction</span></span>
<span data-ttu-id="f74c4-115">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="f74c4-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f74c4-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f74c4-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f74c4-117">Contínuo</span><span class="sxs-lookup"><span data-stu-id="f74c4-117">Continue</span></span>
- <span data-ttu-id="f74c4-118">Ignorar</span><span class="sxs-lookup"><span data-stu-id="f74c4-118">Ignore</span></span>
- <span data-ttu-id="f74c4-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="f74c4-119">Inquire</span></span>
- <span data-ttu-id="f74c4-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f74c4-120">SilentlyContinue</span></span>
- <span data-ttu-id="f74c4-121">Finaliza</span><span class="sxs-lookup"><span data-stu-id="f74c4-121">Stop</span></span>
- <span data-ttu-id="f74c4-122">Suspensão</span><span class="sxs-lookup"><span data-stu-id="f74c4-122">Suspend</span></span>

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

### <span data-ttu-id="f74c4-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f74c4-123">-InformationVariable</span></span>
<span data-ttu-id="f74c4-124">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="f74c4-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f74c4-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f74c4-125">-Profile</span></span>
<span data-ttu-id="f74c4-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f74c4-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f74c4-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f74c4-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f74c4-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="f74c4-128">-PublicIPName</span></span>
<span data-ttu-id="f74c4-129">Especifica o nome do IP público.</span><span class="sxs-lookup"><span data-stu-id="f74c4-129">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74c4-130">-VM</span><span class="sxs-lookup"><span data-stu-id="f74c4-130">-VM</span></span>
<span data-ttu-id="f74c4-131">Especifica a máquina virtual para a qual esse cmdlet obtém configuração de IP público.</span><span class="sxs-lookup"><span data-stu-id="f74c4-131">Specifies the virtual machine for which this cmdlet gets Public IP configuration.</span></span>

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

### <span data-ttu-id="f74c4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f74c4-132">CommonParameters</span></span>
<span data-ttu-id="f74c4-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f74c4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f74c4-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f74c4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f74c4-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f74c4-135">INPUTS</span></span>

## <span data-ttu-id="f74c4-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f74c4-136">OUTPUTS</span></span>

### <span data-ttu-id="f74c4-137">Microsoft. WindowsAzure. Commands. immanagement. AssignPublicIPCollection</span><span class="sxs-lookup"><span data-stu-id="f74c4-137">Microsoft.WindowsAzure.Commands.ServiceManagement.AssignPublicIPCollection</span></span>

## <span data-ttu-id="f74c4-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f74c4-138">NOTES</span></span>

## <span data-ttu-id="f74c4-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f74c4-139">RELATED LINKS</span></span>

[<span data-ttu-id="f74c4-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f74c4-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f74c4-141">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="f74c4-141">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="f74c4-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="f74c4-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)


