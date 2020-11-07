---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C19A1DC0-47FA-4687-B81F-315EA04AD4A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22591c1aa5a670e8f0d73f206ed6d2bcbe52c88f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945494"
---
# <span data-ttu-id="274ca-101">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="274ca-101">Remove-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="274ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="274ca-102">SYNOPSIS</span></span>
<span data-ttu-id="274ca-103">Remove uma extensão do SQL Server do Azure Virtual Machine de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="274ca-103">Removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="274ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="274ca-104">SYNTAX</span></span>

```
Remove-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="274ca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="274ca-105">DESCRIPTION</span></span>
<span data-ttu-id="274ca-106">O cmdlet **Remove-AzureVMSqlServerExtension** remove uma extensão do SQL Server do Azure Virtual Machine de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="274ca-106">The **Remove-AzureVMSqlServerExtension** cmdlet removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="274ca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="274ca-107">EXAMPLES</span></span>

### <span data-ttu-id="274ca-108">1:</span><span class="sxs-lookup"><span data-stu-id="274ca-108">1:</span></span>
```

```

## <span data-ttu-id="274ca-109">OS</span><span class="sxs-lookup"><span data-stu-id="274ca-109">PARAMETERS</span></span>

### <span data-ttu-id="274ca-110">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="274ca-110">-InformationAction</span></span>
<span data-ttu-id="274ca-111">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="274ca-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="274ca-112">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="274ca-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="274ca-113">Contínuo</span><span class="sxs-lookup"><span data-stu-id="274ca-113">Continue</span></span>
- <span data-ttu-id="274ca-114">Ignorar</span><span class="sxs-lookup"><span data-stu-id="274ca-114">Ignore</span></span>
- <span data-ttu-id="274ca-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="274ca-115">Inquire</span></span>
- <span data-ttu-id="274ca-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="274ca-116">SilentlyContinue</span></span>
- <span data-ttu-id="274ca-117">Finaliza</span><span class="sxs-lookup"><span data-stu-id="274ca-117">Stop</span></span>
- <span data-ttu-id="274ca-118">Suspensão</span><span class="sxs-lookup"><span data-stu-id="274ca-118">Suspend</span></span>

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

### <span data-ttu-id="274ca-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="274ca-119">-InformationVariable</span></span>
<span data-ttu-id="274ca-120">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="274ca-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="274ca-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="274ca-121">-Profile</span></span>
<span data-ttu-id="274ca-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="274ca-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="274ca-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="274ca-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="274ca-124">-VM</span><span class="sxs-lookup"><span data-stu-id="274ca-124">-VM</span></span>
<span data-ttu-id="274ca-125">Especifica o objeto da máquina virtual persistente do qual esse cmdlet Remove a extensão.</span><span class="sxs-lookup"><span data-stu-id="274ca-125">Specifies the persistent virtual machine object that this cmdlet removes the extension from.</span></span>

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

### <span data-ttu-id="274ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="274ca-126">CommonParameters</span></span>
<span data-ttu-id="274ca-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="274ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="274ca-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="274ca-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="274ca-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="274ca-129">INPUTS</span></span>

## <span data-ttu-id="274ca-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="274ca-130">OUTPUTS</span></span>

## <span data-ttu-id="274ca-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="274ca-131">NOTES</span></span>

## <span data-ttu-id="274ca-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="274ca-132">RELATED LINKS</span></span>

[<span data-ttu-id="274ca-133">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="274ca-133">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="274ca-134">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="274ca-134">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


