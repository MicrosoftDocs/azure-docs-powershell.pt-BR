---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DBB8EC31-877C-4DB1-8197-CA7A4148AE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f8767c9477db41251eb4732a2eb96d8dd782c20
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945531"
---
# <span data-ttu-id="97c8f-101">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="97c8f-101">Get-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="97c8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="97c8f-103">Obtém informações de uma extensão de script personalizado da máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="97c8f-103">Gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="97c8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97c8f-104">SYNTAX</span></span>

```
Get-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="97c8f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97c8f-105">DESCRIPTION</span></span>
<span data-ttu-id="97c8f-106">O cmdlet **Get-AzureVMCustomScriptExtension** Obtém informações de uma extensão de script personalizado da máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="97c8f-106">The **Get-AzureVMCustomScriptExtension** cmdlet gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="97c8f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97c8f-107">EXAMPLES</span></span>

### <span data-ttu-id="97c8f-108">Exemplo 1: obter uma extensão de script de máquina virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="97c8f-108">Example 1: Get an Azure virtual machine script extension</span></span>
```
PS C:\> Get-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="97c8f-109">Esse comando obtém uma extensão de script da máquina virtual do Azure armazenada na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="97c8f-109">This command gets an Azure virtual machine script extension stored in the variable $VM.</span></span>

## <span data-ttu-id="97c8f-110">OS</span><span class="sxs-lookup"><span data-stu-id="97c8f-110">PARAMETERS</span></span>

### <span data-ttu-id="97c8f-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="97c8f-111">-InformationAction</span></span>
<span data-ttu-id="97c8f-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="97c8f-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="97c8f-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="97c8f-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97c8f-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="97c8f-114">Continue</span></span>
- <span data-ttu-id="97c8f-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="97c8f-115">Ignore</span></span>
- <span data-ttu-id="97c8f-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="97c8f-116">Inquire</span></span>
- <span data-ttu-id="97c8f-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="97c8f-117">SilentlyContinue</span></span>
- <span data-ttu-id="97c8f-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="97c8f-118">Stop</span></span>
- <span data-ttu-id="97c8f-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="97c8f-119">Suspend</span></span>

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

### <span data-ttu-id="97c8f-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="97c8f-120">-InformationVariable</span></span>
<span data-ttu-id="97c8f-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="97c8f-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="97c8f-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="97c8f-122">-Profile</span></span>
<span data-ttu-id="97c8f-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="97c8f-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="97c8f-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="97c8f-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="97c8f-125">-VM</span><span class="sxs-lookup"><span data-stu-id="97c8f-125">-VM</span></span>
<span data-ttu-id="97c8f-126">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="97c8f-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="97c8f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c8f-127">CommonParameters</span></span>
<span data-ttu-id="97c8f-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c8f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c8f-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97c8f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c8f-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97c8f-130">INPUTS</span></span>

## <span data-ttu-id="97c8f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97c8f-131">OUTPUTS</span></span>

## <span data-ttu-id="97c8f-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97c8f-132">NOTES</span></span>

## <span data-ttu-id="97c8f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97c8f-133">RELATED LINKS</span></span>

[<span data-ttu-id="97c8f-134">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="97c8f-134">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="97c8f-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="97c8f-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


