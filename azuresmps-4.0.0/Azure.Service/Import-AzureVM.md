---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946255"
---
# <span data-ttu-id="6b344-101">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6b344-101">Import-AzureVM</span></span>

## <span data-ttu-id="6b344-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b344-102">SYNOPSIS</span></span>
<span data-ttu-id="6b344-103">Importa o estado da máquina virtual do Azure de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6b344-103">Imports an Azure virtual machine state from a file.</span></span>

## <span data-ttu-id="6b344-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b344-104">SYNTAX</span></span>

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b344-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b344-105">DESCRIPTION</span></span>
<span data-ttu-id="6b344-106">O cmdlet **Import-AzureVM** importa o estado salvo anteriormente de uma máquina virtual de um arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="6b344-106">The **Import-AzureVM** cmdlet imports the previously saved state of a virtual machine from an XML file.</span></span>
<span data-ttu-id="6b344-107">Esse cmdlet é útil quando você deseja criar subseqüentemente uma máquina virtual a partir dos dados importados.</span><span class="sxs-lookup"><span data-stu-id="6b344-107">This cmdlet is useful when you want to subsequently create a virtual machine from the imported data.</span></span>

<span data-ttu-id="6b344-108">Executando **Export-AzureVM** , seguido de **Remove-AzureVM** e, em seguida, **Import-AzureVM** para recriar uma máquina virtual pode fazer com que a máquina virtual resultante tenha um endereço IP diferente do original.</span><span class="sxs-lookup"><span data-stu-id="6b344-108">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="6b344-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b344-109">EXAMPLES</span></span>

### <span data-ttu-id="6b344-110">Exemplo 1: importar um estado da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="6b344-110">Example 1: Import a virtual machine state</span></span>
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

<span data-ttu-id="6b344-111">Esse comando importa o estado de uma máquina virtual do arquivo VMstate.xml e, em seguida, cria uma máquina virtual no serviço na nuvem especificado.</span><span class="sxs-lookup"><span data-stu-id="6b344-111">This command imports the state of a virtual machine from the VMstate.xml file, and then creates a virtual machine in the specified cloud service.</span></span>

## <span data-ttu-id="6b344-112">OS</span><span class="sxs-lookup"><span data-stu-id="6b344-112">PARAMETERS</span></span>

### <span data-ttu-id="6b344-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="6b344-113">-InformationAction</span></span>
<span data-ttu-id="6b344-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="6b344-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6b344-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6b344-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b344-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="6b344-116">Continue</span></span>
- <span data-ttu-id="6b344-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="6b344-117">Ignore</span></span>
- <span data-ttu-id="6b344-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="6b344-118">Inquire</span></span>
- <span data-ttu-id="6b344-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6b344-119">SilentlyContinue</span></span>
- <span data-ttu-id="6b344-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="6b344-120">Stop</span></span>
- <span data-ttu-id="6b344-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="6b344-121">Suspend</span></span>

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

### <span data-ttu-id="6b344-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6b344-122">-InformationVariable</span></span>
<span data-ttu-id="6b344-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="6b344-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6b344-124">-Caminho</span><span class="sxs-lookup"><span data-stu-id="6b344-124">-Path</span></span>
<span data-ttu-id="6b344-125">Especifica o caminho do arquivo com o estado da máquina virtual salva anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6b344-125">Specifies the path of the file with the previously saved virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b344-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b344-126">CommonParameters</span></span>
<span data-ttu-id="6b344-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b344-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b344-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b344-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b344-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b344-129">INPUTS</span></span>

## <span data-ttu-id="6b344-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b344-130">OUTPUTS</span></span>

## <span data-ttu-id="6b344-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b344-131">NOTES</span></span>

## <span data-ttu-id="6b344-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b344-132">RELATED LINKS</span></span>

[<span data-ttu-id="6b344-133">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6b344-133">Export-AzureVM</span></span>](./Export-AzureVM.md)

[<span data-ttu-id="6b344-134">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6b344-134">New-AzureVM</span></span>](./New-AzureVM.md)


