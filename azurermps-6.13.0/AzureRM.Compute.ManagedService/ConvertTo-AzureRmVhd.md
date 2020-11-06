---
external help file: AzureRM.Compute.ManagedService-help.xml
Module Name: AzureRM.Compute.ManagedService
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: 0fa0f2d5cb78fe96f05b818b5cbfdabca47cbdee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427271"
---
# <span data-ttu-id="6037d-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="6037d-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="6037d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6037d-102">SYNOPSIS</span></span>
<span data-ttu-id="6037d-103">Converter o Hyper-V VM para o Azure oferece suporte a arquivos de disco rígido virtual</span><span class="sxs-lookup"><span data-stu-id="6037d-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6037d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6037d-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6037d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6037d-105">DESCRIPTION</span></span>
<span data-ttu-id="6037d-106">Converter o Hyper-V VM para o Azure oferece suporte a arquivos de disco rígido virtual</span><span class="sxs-lookup"><span data-stu-id="6037d-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="6037d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6037d-107">EXAMPLES</span></span>

### <span data-ttu-id="6037d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6037d-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="6037d-109">Converta o Hyper-V VM chamado ' test ' para o Azure com suporte para os arquivos de disco rígido virtual para a pasta atual.</span><span class="sxs-lookup"><span data-stu-id="6037d-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="6037d-110">OS</span><span class="sxs-lookup"><span data-stu-id="6037d-110">PARAMETERS</span></span>

### <span data-ttu-id="6037d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6037d-111">-AsJob</span></span>
<span data-ttu-id="6037d-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="6037d-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6037d-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="6037d-113">-ExportPath</span></span>
<span data-ttu-id="6037d-114">O caminho da pasta de exportação que conterá os arquivos de disco.</span><span class="sxs-lookup"><span data-stu-id="6037d-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6037d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6037d-115">-Force</span></span>
<span data-ttu-id="6037d-116">Force a exportação mesmo se a pasta existente for encontrada.</span><span class="sxs-lookup"><span data-stu-id="6037d-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6037d-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="6037d-117">-HyperVServer</span></span>
<span data-ttu-id="6037d-118">O nome DNS do servidor Hyper-V, com ' localhost ' como o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="6037d-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6037d-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="6037d-119">-HyperVVMName</span></span>
<span data-ttu-id="6037d-120">O nome do nome do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="6037d-120">The Hyper-V name name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6037d-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6037d-121">-Confirm</span></span>
<span data-ttu-id="6037d-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6037d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6037d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6037d-123">-WhatIf</span></span>
<span data-ttu-id="6037d-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6037d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6037d-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6037d-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6037d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6037d-126">CommonParameters</span></span>
<span data-ttu-id="6037d-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6037d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6037d-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6037d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6037d-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6037d-129">INPUTS</span></span>

### <span data-ttu-id="6037d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6037d-130">System.String</span></span>

## <span data-ttu-id="6037d-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6037d-131">OUTPUTS</span></span>

### <span data-ttu-id="6037d-132">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="6037d-132">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="6037d-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6037d-133">NOTES</span></span>

## <span data-ttu-id="6037d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6037d-134">RELATED LINKS</span></span>
