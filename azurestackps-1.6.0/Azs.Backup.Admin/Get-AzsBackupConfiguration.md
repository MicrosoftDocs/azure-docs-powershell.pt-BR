---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 500a8e28ceb4eb452d788574b8a80865b5e54b14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426110"
---
# <span data-ttu-id="adcc9-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="adcc9-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="adcc9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adcc9-102">SYNOPSIS</span></span>
<span data-ttu-id="adcc9-103">Retorna a lista de configurações de backup.</span><span class="sxs-lookup"><span data-stu-id="adcc9-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="adcc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adcc9-104">SYNTAX</span></span>

### <span data-ttu-id="adcc9-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="adcc9-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="adcc9-106">Obter</span><span class="sxs-lookup"><span data-stu-id="adcc9-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="adcc9-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="adcc9-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="adcc9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="adcc9-108">DESCRIPTION</span></span>
<span data-ttu-id="adcc9-109">Retorna a lista de configurações de backup.</span><span class="sxs-lookup"><span data-stu-id="adcc9-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="adcc9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="adcc9-110">EXAMPLES</span></span>

### <span data-ttu-id="adcc9-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="adcc9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="adcc9-112">Obtenha a configuração de backup do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="adcc9-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="adcc9-113">OS</span><span class="sxs-lookup"><span data-stu-id="adcc9-113">PARAMETERS</span></span>

### <span data-ttu-id="adcc9-114">-Local</span><span class="sxs-lookup"><span data-stu-id="adcc9-114">-Location</span></span>
<span data-ttu-id="adcc9-115">Local de backup.</span><span class="sxs-lookup"><span data-stu-id="adcc9-115">Backup location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adcc9-116">-ResourceGroupName</span></span>
<span data-ttu-id="adcc9-117">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="adcc9-117">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc9-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adcc9-118">-ResourceId</span></span>
<span data-ttu-id="adcc9-119">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="adcc9-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adcc9-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="adcc9-120">-Skip</span></span>
<span data-ttu-id="adcc9-121">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="adcc9-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc9-122">-Início</span><span class="sxs-lookup"><span data-stu-id="adcc9-122">-Top</span></span>
<span data-ttu-id="adcc9-123">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="adcc9-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="adcc9-124">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="adcc9-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adcc9-125">CommonParameters</span></span>
<span data-ttu-id="adcc9-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adcc9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adcc9-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adcc9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adcc9-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="adcc9-128">INPUTS</span></span>

## <span data-ttu-id="adcc9-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="adcc9-129">OUTPUTS</span></span>

### <span data-ttu-id="adcc9-130">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="adcc9-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="adcc9-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="adcc9-131">NOTES</span></span>

## <span data-ttu-id="adcc9-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adcc9-132">RELATED LINKS</span></span>

