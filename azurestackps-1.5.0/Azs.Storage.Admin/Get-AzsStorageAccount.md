---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: be2198103338a3df56f924e28b497095e21bf1de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601780"
---
# <span data-ttu-id="6d788-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d788-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="6d788-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d788-102">SYNOPSIS</span></span>
<span data-ttu-id="6d788-103">Retorna a conta de armazenamento solicitada.</span><span class="sxs-lookup"><span data-stu-id="6d788-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="6d788-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d788-104">SYNTAX</span></span>

### <span data-ttu-id="6d788-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="6d788-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6d788-106">Obter</span><span class="sxs-lookup"><span data-stu-id="6d788-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="6d788-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="6d788-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="6d788-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d788-108">DESCRIPTION</span></span>
<span data-ttu-id="6d788-109">Retorna a conta de armazenamento solicitada.</span><span class="sxs-lookup"><span data-stu-id="6d788-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="6d788-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d788-110">EXAMPLES</span></span>

### <span data-ttu-id="6d788-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6d788-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="6d788-112">Obter uma lista de contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6d788-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="6d788-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6d788-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="6d788-114">Obter detalhes da conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="6d788-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="6d788-115">OS</span><span class="sxs-lookup"><span data-stu-id="6d788-115">PARAMETERS</span></span>

### <span data-ttu-id="6d788-116">-Farmname</span><span class="sxs-lookup"><span data-stu-id="6d788-116">-FarmName</span></span>
<span data-ttu-id="6d788-117">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="6d788-117">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d788-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d788-118">-Name</span></span>
<span data-ttu-id="6d788-119">ID da conta de armazenamento interna, que não está visível para Tenant.</span><span class="sxs-lookup"><span data-stu-id="6d788-119">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d788-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d788-120">-ResourceGroupName</span></span>
<span data-ttu-id="6d788-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d788-121">Resource group name.</span></span>

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

### <span data-ttu-id="6d788-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d788-122">-ResourceId</span></span>
<span data-ttu-id="6d788-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="6d788-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d788-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="6d788-124">-Skip</span></span>
<span data-ttu-id="6d788-125">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6d788-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6d788-126">-Resumo</span><span class="sxs-lookup"><span data-stu-id="6d788-126">-Summary</span></span>
<span data-ttu-id="6d788-127">A opção de resumo wheter ou informações detalhadas são retornadas.</span><span class="sxs-lookup"><span data-stu-id="6d788-127">Switch for wheter summary or detailed information is returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d788-128">-Início</span><span class="sxs-lookup"><span data-stu-id="6d788-128">-Top</span></span>
<span data-ttu-id="6d788-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6d788-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6d788-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="6d788-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6d788-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d788-131">CommonParameters</span></span>
<span data-ttu-id="6d788-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d788-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d788-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d788-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d788-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d788-134">INPUTS</span></span>

## <span data-ttu-id="6d788-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d788-135">OUTPUTS</span></span>

### <span data-ttu-id="6d788-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d788-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="6d788-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d788-137">NOTES</span></span>

## <span data-ttu-id="6d788-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d788-138">RELATED LINKS</span></span>

