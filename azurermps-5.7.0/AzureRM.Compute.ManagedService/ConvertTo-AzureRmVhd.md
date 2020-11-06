---
external help file: ''
Module Name: ''
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: c440fa43a4e15abb5ab9f87d5b814fe3cbc55d63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428991"
---
# <span data-ttu-id="28ec9-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="28ec9-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="28ec9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="28ec9-103">Converter o Hyper-V VM para o Azure oferece suporte a arquivos de disco rígido virtual</span><span class="sxs-lookup"><span data-stu-id="28ec9-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28ec9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28ec9-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="28ec9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28ec9-105">DESCRIPTION</span></span>
<span data-ttu-id="28ec9-106">Converter o Hyper-V VM para o Azure oferece suporte a arquivos de disco rígido virtual</span><span class="sxs-lookup"><span data-stu-id="28ec9-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="28ec9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28ec9-107">EXAMPLES</span></span>

### <span data-ttu-id="28ec9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28ec9-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="28ec9-109">Converta o Hyper-V VM chamado ' test ' para o Azure com suporte para os arquivos de disco rígido virtual para a pasta atual.</span><span class="sxs-lookup"><span data-stu-id="28ec9-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="28ec9-110">OS</span><span class="sxs-lookup"><span data-stu-id="28ec9-110">PARAMETERS</span></span>

### <span data-ttu-id="28ec9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28ec9-111">-AsJob</span></span>
<span data-ttu-id="28ec9-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="28ec9-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ec9-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="28ec9-113">-ExportPath</span></span>
<span data-ttu-id="28ec9-114">O caminho da pasta de exportação que conterá os arquivos de disco.</span><span class="sxs-lookup"><span data-stu-id="28ec9-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ec9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="28ec9-115">-Force</span></span>
<span data-ttu-id="28ec9-116">Force a exportação mesmo se a pasta existente for encontrada.</span><span class="sxs-lookup"><span data-stu-id="28ec9-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ec9-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="28ec9-117">-HyperVServer</span></span>
<span data-ttu-id="28ec9-118">O nome DNS do servidor Hyper-V, com ' localhost ' como o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="28ec9-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ec9-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="28ec9-119">-HyperVVMName</span></span>
<span data-ttu-id="28ec9-120">O nome do nome do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="28ec9-120">The Hyper-V name name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ec9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ec9-121">CommonParameters</span></span>
<span data-ttu-id="28ec9-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28ec9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ec9-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28ec9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ec9-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28ec9-124">INPUTS</span></span>

### <span data-ttu-id="28ec9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="28ec9-125">System.String</span></span>

## <span data-ttu-id="28ec9-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28ec9-126">OUTPUTS</span></span>

### <span data-ttu-id="28ec9-127">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="28ec9-127">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="28ec9-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28ec9-128">NOTES</span></span>

## <span data-ttu-id="28ec9-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28ec9-129">RELATED LINKS</span></span>

