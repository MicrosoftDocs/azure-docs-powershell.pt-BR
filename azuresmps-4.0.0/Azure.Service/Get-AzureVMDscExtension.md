---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9D6D1890-9442-45F1-A3AA-BB1DB5CB33D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 462d40e463edf6894810ac6e00e39b9c7a9eabe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946538"
---
# <span data-ttu-id="72ac2-101">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="72ac2-101">Get-AzureVMDscExtension</span></span>

## <span data-ttu-id="72ac2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="72ac2-103">Obtém as configurações da extensão DSC em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="72ac2-103">Gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="72ac2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72ac2-104">SYNTAX</span></span>

```
Get-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="72ac2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72ac2-105">DESCRIPTION</span></span>
<span data-ttu-id="72ac2-106">O cmdlet **Get-AzureVMDscExtension** Obtém as configurações da extensão DSC em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="72ac2-106">The **Get-AzureVMDscExtension** cmdlet gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="72ac2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72ac2-107">EXAMPLES</span></span>

### <span data-ttu-id="72ac2-108">Exemplo 1: obter a configuração da extensão DSC em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="72ac2-108">Example 1: Get the setting of the DSC Extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMDscExtension -VM $VMModulesUrl
https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zipConfigurationFunction : MyConfiguration.ps1\MyConfigurationProperties            : {ServerName}ExtensionName         : DSCPublisher             : Microsoft.PowershellVersion               : 1.*PrivateConfiguration  :PublicConfiguration   : {"ModulesUrl": "https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zip","ConfigurationFunction": "MyConfiguration.ps1\\MyConfiguration","Properties": {"ServerName": "C:\\MyDirectory"}}ReferenceName         : DSCState                 : EnableRoleName              : my-vm
```

<span data-ttu-id="72ac2-109">Esse comando obtém as configurações da extensão DSC em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="72ac2-109">This command gets the settings of the DSC Extension on a virtual machine.</span></span>

## <span data-ttu-id="72ac2-110">OS</span><span class="sxs-lookup"><span data-stu-id="72ac2-110">PARAMETERS</span></span>

### <span data-ttu-id="72ac2-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="72ac2-111">-InformationAction</span></span>
<span data-ttu-id="72ac2-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="72ac2-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="72ac2-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="72ac2-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="72ac2-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="72ac2-114">Continue</span></span>
- <span data-ttu-id="72ac2-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="72ac2-115">Ignore</span></span>
- <span data-ttu-id="72ac2-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="72ac2-116">Inquire</span></span>
- <span data-ttu-id="72ac2-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="72ac2-117">SilentlyContinue</span></span>
- <span data-ttu-id="72ac2-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="72ac2-118">Stop</span></span>
- <span data-ttu-id="72ac2-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="72ac2-119">Suspend</span></span>

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

### <span data-ttu-id="72ac2-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="72ac2-120">-InformationVariable</span></span>
<span data-ttu-id="72ac2-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="72ac2-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="72ac2-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="72ac2-122">-Profile</span></span>
<span data-ttu-id="72ac2-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="72ac2-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="72ac2-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="72ac2-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="72ac2-125">-VM</span><span class="sxs-lookup"><span data-stu-id="72ac2-125">-VM</span></span>
<span data-ttu-id="72ac2-126">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="72ac2-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="72ac2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ac2-127">CommonParameters</span></span>
<span data-ttu-id="72ac2-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72ac2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ac2-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72ac2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ac2-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72ac2-130">INPUTS</span></span>

## <span data-ttu-id="72ac2-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72ac2-131">OUTPUTS</span></span>

### <span data-ttu-id="72ac2-132">Microsoft. WindowsAzure. Commands. onmanagement. IaaS. Extensions. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="72ac2-132">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="72ac2-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72ac2-133">NOTES</span></span>

## <span data-ttu-id="72ac2-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72ac2-134">RELATED LINKS</span></span>

[<span data-ttu-id="72ac2-135">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="72ac2-135">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="72ac2-136">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="72ac2-136">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="72ac2-137">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="72ac2-137">Get-AzureVMDscExtensionStatus</span></span>](./Get-AzureVMDscExtensionStatus.md)


