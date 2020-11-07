---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1E1F98E9-FC45-4BEF-90F6-A21D7DB7C82F
online version: ''
schema: 2.0.0
ms.openlocfilehash: eac6db4400e5c51f295e0bbf549117ffdbc97644
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946445"
---
# <span data-ttu-id="a587c-101">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="a587c-101">Remove-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="a587c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a587c-102">SYNOPSIS</span></span>
<span data-ttu-id="a587c-103">Remove a configuração de disco do sistema operacional do objeto DiskConfigSet.</span><span class="sxs-lookup"><span data-stu-id="a587c-103">Removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="a587c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a587c-104">SYNTAX</span></span>

```
Remove-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a587c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a587c-105">DESCRIPTION</span></span>
<span data-ttu-id="a587c-106">O cmdlet **Remove-AzureVMImageOSDiskConfig** remove a configuração de disco do sistema operacional do objeto DiskConfigSet.</span><span class="sxs-lookup"><span data-stu-id="a587c-106">The **Remove-AzureVMImageOSDiskConfig** cmdlet removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="a587c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a587c-107">EXAMPLES</span></span>

### <span data-ttu-id="a587c-108">Exemplo 1: remover a configuração de disco do sistema operacional de um DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="a587c-108">Example 1: Remove the operating system disk configuration from a DiskConfigSet</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageOSDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="a587c-109">Este comando Remove a configuração de disco do sistema operacional do objeto DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="a587c-109">This command removes the operating system disk configuration from the DiskConfigSet object</span></span>

## <span data-ttu-id="a587c-110">OS</span><span class="sxs-lookup"><span data-stu-id="a587c-110">PARAMETERS</span></span>

### <span data-ttu-id="a587c-111">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="a587c-111">-DiskConfig</span></span>
<span data-ttu-id="a587c-112">Especifica o objeto de configuração de disco que encapsula o disco do sistema operacional e os objetos de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="a587c-112">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a587c-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a587c-113">-InformationAction</span></span>
<span data-ttu-id="a587c-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="a587c-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a587c-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a587c-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a587c-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="a587c-116">Continue</span></span>
- <span data-ttu-id="a587c-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="a587c-117">Ignore</span></span>
- <span data-ttu-id="a587c-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="a587c-118">Inquire</span></span>
- <span data-ttu-id="a587c-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a587c-119">SilentlyContinue</span></span>
- <span data-ttu-id="a587c-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="a587c-120">Stop</span></span>
- <span data-ttu-id="a587c-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="a587c-121">Suspend</span></span>

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

### <span data-ttu-id="a587c-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a587c-122">-InformationVariable</span></span>
<span data-ttu-id="a587c-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="a587c-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a587c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a587c-124">CommonParameters</span></span>
<span data-ttu-id="a587c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a587c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a587c-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a587c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a587c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a587c-127">INPUTS</span></span>

## <span data-ttu-id="a587c-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a587c-128">OUTPUTS</span></span>

### <span data-ttu-id="a587c-129">Microsoft. WindowsAzure. Commands. onmanagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="a587c-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="a587c-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a587c-130">NOTES</span></span>

## <span data-ttu-id="a587c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a587c-131">RELATED LINKS</span></span>

[<span data-ttu-id="a587c-132">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="a587c-132">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)


