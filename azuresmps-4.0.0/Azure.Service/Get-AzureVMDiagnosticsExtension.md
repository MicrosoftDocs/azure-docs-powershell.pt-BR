---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E1A3FF-E479-44CD-8147-15408DF3F79A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f8290b0e4f40305495b535b28b2a8f61d7911ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946543"
---
# <span data-ttu-id="9d135-101">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9d135-101">Get-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="9d135-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d135-102">SYNOPSIS</span></span>
<span data-ttu-id="9d135-103">Obtém as configurações da extensão de diagnóstico do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d135-103">Gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="9d135-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d135-104">SYNTAX</span></span>

```
Get-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9d135-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d135-105">DESCRIPTION</span></span>
<span data-ttu-id="9d135-106">O cmdlet **Get-AzureVMDiagnosticsExtension** Obtém as configurações da extensão de diagnóstico do Microsoft Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d135-106">The **Get-AzureVMDiagnosticsExtension** cmdlet gets the settings of the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="9d135-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d135-107">EXAMPLES</span></span>

### <span data-ttu-id="9d135-108">Exemplo 1: obter a extensão do diagnóstico aplicada a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="9d135-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVMDiagnosticsExtension -VM $VM
```

<span data-ttu-id="9d135-109">Esse comando obtém a extensão de diagnóstico aplicada à máquina virtual especificada, conforme armazenada na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="9d135-109">This command gets the diagnostics extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="9d135-110">OS</span><span class="sxs-lookup"><span data-stu-id="9d135-110">PARAMETERS</span></span>

### <span data-ttu-id="9d135-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9d135-111">-InformationAction</span></span>
<span data-ttu-id="9d135-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="9d135-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9d135-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9d135-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9d135-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="9d135-114">Continue</span></span>
- <span data-ttu-id="9d135-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="9d135-115">Ignore</span></span>
- <span data-ttu-id="9d135-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="9d135-116">Inquire</span></span>
- <span data-ttu-id="9d135-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9d135-117">SilentlyContinue</span></span>
- <span data-ttu-id="9d135-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="9d135-118">Stop</span></span>
- <span data-ttu-id="9d135-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="9d135-119">Suspend</span></span>

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

### <span data-ttu-id="9d135-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9d135-120">-InformationVariable</span></span>
<span data-ttu-id="9d135-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="9d135-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9d135-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9d135-122">-Profile</span></span>
<span data-ttu-id="9d135-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9d135-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d135-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9d135-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d135-125">-VM</span><span class="sxs-lookup"><span data-stu-id="9d135-125">-VM</span></span>
<span data-ttu-id="9d135-126">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="9d135-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="9d135-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d135-127">CommonParameters</span></span>
<span data-ttu-id="9d135-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d135-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d135-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d135-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d135-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d135-130">INPUTS</span></span>

## <span data-ttu-id="9d135-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d135-131">OUTPUTS</span></span>

## <span data-ttu-id="9d135-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d135-132">NOTES</span></span>

## <span data-ttu-id="9d135-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d135-133">RELATED LINKS</span></span>

[<span data-ttu-id="9d135-134">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9d135-134">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="9d135-135">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9d135-135">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)


