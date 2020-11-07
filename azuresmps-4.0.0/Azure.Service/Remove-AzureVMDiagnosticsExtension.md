---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A513B7CA-182E-46A2-8181-020C5DFC7DE9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 316e7c182025171d2f1ba66ead1a0c0f5de120b1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945504"
---
# <span data-ttu-id="f2474-101">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="f2474-101">Remove-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="f2474-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2474-102">SYNOPSIS</span></span>
<span data-ttu-id="f2474-103">Remove a extensão de diagnóstico do Azure de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f2474-103">Removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="f2474-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2474-104">SYNTAX</span></span>

```
Remove-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f2474-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2474-105">DESCRIPTION</span></span>
<span data-ttu-id="f2474-106">O cmdlet **Remove-AzureVMDiagnosticsExtension** remove uma extensão de diagnóstico do Microsoft Azure de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f2474-106">The **Remove-AzureVMDiagnosticsExtension** cmdlet removes a Microsoft Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="f2474-107">Você deve passar a saída deste cmdlet para o cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="f2474-107">You must pass the output of this cmdlet to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="f2474-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2474-108">EXAMPLES</span></span>

### <span data-ttu-id="f2474-109">Exemplo 1: remover a extensão de diagnóstico do Azure de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="f2474-109">Example 1: Remove the Azure Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDiagnosticsExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="f2474-110">Esse comando Remove a extensão de diagnóstico do Azure de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f2474-110">This command removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="f2474-111">OS</span><span class="sxs-lookup"><span data-stu-id="f2474-111">PARAMETERS</span></span>

### <span data-ttu-id="f2474-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f2474-112">-InformationAction</span></span>
<span data-ttu-id="f2474-113">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="f2474-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f2474-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f2474-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2474-115">Contínuo</span><span class="sxs-lookup"><span data-stu-id="f2474-115">Continue</span></span>
- <span data-ttu-id="f2474-116">Ignorar</span><span class="sxs-lookup"><span data-stu-id="f2474-116">Ignore</span></span>
- <span data-ttu-id="f2474-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="f2474-117">Inquire</span></span>
- <span data-ttu-id="f2474-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f2474-118">SilentlyContinue</span></span>
- <span data-ttu-id="f2474-119">Finaliza</span><span class="sxs-lookup"><span data-stu-id="f2474-119">Stop</span></span>
- <span data-ttu-id="f2474-120">Suspensão</span><span class="sxs-lookup"><span data-stu-id="f2474-120">Suspend</span></span>

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

### <span data-ttu-id="f2474-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f2474-121">-InformationVariable</span></span>
<span data-ttu-id="f2474-122">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="f2474-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f2474-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f2474-123">-Profile</span></span>
<span data-ttu-id="f2474-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f2474-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2474-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f2474-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2474-126">-VM</span><span class="sxs-lookup"><span data-stu-id="f2474-126">-VM</span></span>
<span data-ttu-id="f2474-127">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="f2474-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="f2474-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2474-128">CommonParameters</span></span>
<span data-ttu-id="f2474-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2474-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2474-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2474-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2474-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2474-131">INPUTS</span></span>

## <span data-ttu-id="f2474-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2474-132">OUTPUTS</span></span>

## <span data-ttu-id="f2474-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2474-133">NOTES</span></span>

## <span data-ttu-id="f2474-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2474-134">RELATED LINKS</span></span>

[<span data-ttu-id="f2474-135">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="f2474-135">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="f2474-136">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="f2474-136">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="f2474-137">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f2474-137">Update-AzureVM</span></span>](./Update-AzureVM.md)


