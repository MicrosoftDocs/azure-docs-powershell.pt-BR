---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0093393f926af257e07b7d697a7f267fa62b483a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427052"
---
# <span data-ttu-id="07762-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="07762-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="07762-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07762-102">SYNOPSIS</span></span>
<span data-ttu-id="07762-103">Cria um novo servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="07762-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07762-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07762-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07762-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07762-105">DESCRIPTION</span></span>
<span data-ttu-id="07762-106">O cmdlet New-AzureRmAnalysisServicesServer cria um novo servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="07762-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="07762-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07762-107">EXAMPLES</span></span>

### <span data-ttu-id="07762-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07762-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="07762-109">Cria um servidor chamado TestServer na região do Azure West-US e no grupo de recursos testresrourcegroup.</span><span class="sxs-lookup"><span data-stu-id="07762-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="07762-110">O nível de SKU do servidor será S1.</span><span class="sxs-lookup"><span data-stu-id="07762-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="07762-111">OS</span><span class="sxs-lookup"><span data-stu-id="07762-111">PARAMETERS</span></span>

### <span data-ttu-id="07762-112">-Administrador</span><span class="sxs-lookup"><span data-stu-id="07762-112">-Administrator</span></span>
<span data-ttu-id="07762-113">Uma cadeia de caracteres que representa uma lista separada por vírgulas de usuários ou grupos a serem definidos como administradores no servidor.</span><span class="sxs-lookup"><span data-stu-id="07762-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="07762-114">Os usuários ou grupos precisam ser do formato UPN especificado, por exemplo, user@contoso.com ou groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="07762-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07762-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="07762-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="07762-116">O URI do contêiner de BLOB para fazer backup do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="07762-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07762-117">-Local</span><span class="sxs-lookup"><span data-stu-id="07762-117">-Location</span></span>
<span data-ttu-id="07762-118">A região do Azure na qual o servidor do Analysis Services está hospedado</span><span class="sxs-lookup"><span data-stu-id="07762-118">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: North Central US, South Central US, Central US, West Europe, North Europe, West US, East US, East US 2, Japan East, Japan West, Brazil South, Southeast Asia, East Asia, Australia East, Australia Southeast

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07762-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="07762-119">-Name</span></span>
<span data-ttu-id="07762-120">Nome do servidor do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="07762-120">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07762-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07762-121">-ResourceGroupName</span></span>
<span data-ttu-id="07762-122">Nome do grupo de recursos do Azure ao qual o servidor pertence</span><span class="sxs-lookup"><span data-stu-id="07762-122">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="07762-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="07762-123">-Sku</span></span>
<span data-ttu-id="07762-124">O nome da SKU do servidor.</span><span class="sxs-lookup"><span data-stu-id="07762-124">The name of the Sku for the server.</span></span>
<span data-ttu-id="07762-125">Os valores compatíveis são 0 ', 1 ', 2 ' são 4 ' para o nível padrão; ' B1 ', ' B2 ' para a camada básica e 1 ' para o nível de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="07762-125">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07762-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="07762-126">-Tag</span></span>
<span data-ttu-id="07762-127">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="07762-127">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07762-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="07762-128">-Confirm</span></span>
<span data-ttu-id="07762-129">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="07762-129">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07762-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07762-130">-WhatIf</span></span>
<span data-ttu-id="07762-131">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="07762-131">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07762-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07762-132">CommonParameters</span></span>
<span data-ttu-id="07762-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07762-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07762-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07762-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07762-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07762-135">INPUTS</span></span>

## <span data-ttu-id="07762-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07762-136">OUTPUTS</span></span>

### <span data-ttu-id="07762-137">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="07762-137">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="07762-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07762-138">NOTES</span></span>
<span data-ttu-id="07762-139">Alias: New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="07762-139">Alias: New-AzureAs</span></span>

## <span data-ttu-id="07762-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07762-140">RELATED LINKS</span></span>

[<span data-ttu-id="07762-141">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="07762-141">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="07762-142">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="07762-142">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
