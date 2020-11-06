---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: f4b29849109959a8b06a8d0339c8927b8a840a7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602757"
---
# <span data-ttu-id="5d801-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="5d801-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="5d801-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d801-102">SYNOPSIS</span></span>
<span data-ttu-id="5d801-103">Obtém um arquivo. rdp.</span><span class="sxs-lookup"><span data-stu-id="5d801-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d801-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d801-104">SYNTAX</span></span>

### <span data-ttu-id="5d801-105">Downloads</span><span class="sxs-lookup"><span data-stu-id="5d801-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [<CommonParameters>]
```

### <span data-ttu-id="5d801-106">Carregar</span><span class="sxs-lookup"><span data-stu-id="5d801-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [<CommonParameters>]
```

## <span data-ttu-id="5d801-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d801-107">DESCRIPTION</span></span>
<span data-ttu-id="5d801-108">O cmdlet **Get-AzureRmRemoteDesktopFile** Obtém um arquivo de protocolo de área de trabalho remota (. RDP).</span><span class="sxs-lookup"><span data-stu-id="5d801-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="5d801-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d801-109">EXAMPLES</span></span>

### <span data-ttu-id="5d801-110">Exemplo 1: obter um arquivo de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="5d801-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="5d801-111">Esse comando obtém o arquivo da área de trabalho remota para a máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="5d801-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="5d801-112">O comando armazena o resultado no arquivo chamado D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="5d801-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="5d801-113">OS</span><span class="sxs-lookup"><span data-stu-id="5d801-113">PARAMETERS</span></span>

### <span data-ttu-id="5d801-114">-Iniciar</span><span class="sxs-lookup"><span data-stu-id="5d801-114">-Launch</span></span>
<span data-ttu-id="5d801-115">Indica que esse cmdlet inicia a área de trabalho remota depois de obter o arquivo. rdp.</span><span class="sxs-lookup"><span data-stu-id="5d801-115">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d801-116">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="5d801-116">-LocalPath</span></span>
<span data-ttu-id="5d801-117">Especifica o caminho completo local em que esse cmdlet armazena o arquivo. rdp.</span><span class="sxs-lookup"><span data-stu-id="5d801-117">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d801-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d801-118">-Name</span></span>
<span data-ttu-id="5d801-119">Especifica o nome do conjunto de disponibilidade que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="5d801-119">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d801-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d801-120">-ResourceGroupName</span></span>
<span data-ttu-id="5d801-121">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d801-121">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d801-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d801-122">CommonParameters</span></span>
<span data-ttu-id="5d801-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d801-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d801-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d801-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d801-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d801-125">INPUTS</span></span>

### <span data-ttu-id="5d801-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5d801-126">None</span></span>
<span data-ttu-id="5d801-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5d801-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d801-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d801-128">OUTPUTS</span></span>

## <span data-ttu-id="5d801-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d801-129">NOTES</span></span>

## <span data-ttu-id="5d801-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d801-130">RELATED LINKS</span></span>

