---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9EA98944-1923-4573-991E-3B9CA21004BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f16b51dc8abf5c6243b4b489789d65029acc3c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946148"
---
# <span data-ttu-id="83ce7-101">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="83ce7-101">Remove-AzurePublicIP</span></span>

## <span data-ttu-id="83ce7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="83ce7-103">Remove a configuração de IP público de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="83ce7-103">Removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="83ce7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83ce7-104">SYNTAX</span></span>

```
Remove-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="83ce7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="83ce7-106">O cmdlet **Remove-AzurePublicIP** remove a configuração de IP público de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="83ce7-106">The **Remove-AzurePublicIP** cmdlet removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="83ce7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83ce7-107">EXAMPLES</span></span>

### <span data-ttu-id="83ce7-108">Exemplo 1: remover a configuração de IP público</span><span class="sxs-lookup"><span data-stu-id="83ce7-108">Example 1: Remove Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Remove-AzurePublicIP | Update-AzureVM
```

<span data-ttu-id="83ce7-109">Esse comando obtém a máquina virtual chamada FTPInstance no serviço chamado FTPInAzure usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="83ce7-109">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="83ce7-110">O comando transmite a máquina virtual para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="83ce7-110">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="83ce7-111">O cmdlet atual remove a configuração de IP público da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="83ce7-111">The current cmdlet removes Public IP configuration from the virtual machine.</span></span>
<span data-ttu-id="83ce7-112">O comando passa a máquina virtual para o cmdlet **Update-AzureVM** , que implementa suas alterações.</span><span class="sxs-lookup"><span data-stu-id="83ce7-112">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="83ce7-113">OS</span><span class="sxs-lookup"><span data-stu-id="83ce7-113">PARAMETERS</span></span>

### <span data-ttu-id="83ce7-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="83ce7-114">-InformationAction</span></span>
<span data-ttu-id="83ce7-115">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="83ce7-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="83ce7-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="83ce7-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="83ce7-117">Contínuo</span><span class="sxs-lookup"><span data-stu-id="83ce7-117">Continue</span></span>
- <span data-ttu-id="83ce7-118">Ignorar</span><span class="sxs-lookup"><span data-stu-id="83ce7-118">Ignore</span></span>
- <span data-ttu-id="83ce7-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="83ce7-119">Inquire</span></span>
- <span data-ttu-id="83ce7-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="83ce7-120">SilentlyContinue</span></span>
- <span data-ttu-id="83ce7-121">Finaliza</span><span class="sxs-lookup"><span data-stu-id="83ce7-121">Stop</span></span>
- <span data-ttu-id="83ce7-122">Suspensão</span><span class="sxs-lookup"><span data-stu-id="83ce7-122">Suspend</span></span>

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

### <span data-ttu-id="83ce7-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="83ce7-123">-InformationVariable</span></span>
<span data-ttu-id="83ce7-124">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="83ce7-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="83ce7-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="83ce7-125">-Profile</span></span>
<span data-ttu-id="83ce7-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="83ce7-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="83ce7-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="83ce7-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="83ce7-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="83ce7-128">-PublicIPName</span></span>
<span data-ttu-id="83ce7-129">Especifica o nome do IP público.</span><span class="sxs-lookup"><span data-stu-id="83ce7-129">Specifies the Public IP name.</span></span>

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

### <span data-ttu-id="83ce7-130">-VM</span><span class="sxs-lookup"><span data-stu-id="83ce7-130">-VM</span></span>
<span data-ttu-id="83ce7-131">Especifica a máquina virtual a partir da qual esse cmdlet Remove a configuração de IP público.</span><span class="sxs-lookup"><span data-stu-id="83ce7-131">Specifies the virtual machine from which this cmdlet removes Public IP configuration.</span></span>

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

### <span data-ttu-id="83ce7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ce7-132">CommonParameters</span></span>
<span data-ttu-id="83ce7-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ce7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ce7-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83ce7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ce7-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83ce7-135">INPUTS</span></span>

## <span data-ttu-id="83ce7-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83ce7-136">OUTPUTS</span></span>

### <span data-ttu-id="83ce7-137">Microsoft. WindowsAzure. Commands. onmanagement. Model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="83ce7-137">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="83ce7-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83ce7-138">NOTES</span></span>

## <span data-ttu-id="83ce7-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83ce7-139">RELATED LINKS</span></span>

[<span data-ttu-id="83ce7-140">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="83ce7-140">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="83ce7-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="83ce7-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="83ce7-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="83ce7-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)

[<span data-ttu-id="83ce7-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="83ce7-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


