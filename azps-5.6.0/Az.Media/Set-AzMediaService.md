---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: 410b1c87832b4debdfd50cbe6adf27326f12a303
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889260"
---
# <span data-ttu-id="20a2e-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="20a2e-101">Set-AzMediaService</span></span>

## <span data-ttu-id="20a2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="20a2e-103">Modifica as propriedades especificadas de um serviço de mídia existente.</span><span class="sxs-lookup"><span data-stu-id="20a2e-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="20a2e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="20a2e-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20a2e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="20a2e-105">DESCRIPTION</span></span>
<span data-ttu-id="20a2e-106">O cmdlet **Set-AzMediaService** modifica as propriedades especificadas de um serviço de mídia existente.</span><span class="sxs-lookup"><span data-stu-id="20a2e-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="20a2e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20a2e-107">EXAMPLES</span></span>

### <span data-ttu-id="20a2e-108">Exemplo 1: Modificar um serviço de mídia existente</span><span class="sxs-lookup"><span data-stu-id="20a2e-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="20a2e-109">O primeiro comando cria uma série de marcas e armazena essas marcas na variável chamada $Tags.</span><span class="sxs-lookup"><span data-stu-id="20a2e-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="20a2e-110">Este segundo comando atualiza o serviço de mídia chamado MediaService001 que pertence ao grupo de recursos chamado ResourceGroup123 com as marcas armazenadas $Tags variável.</span><span class="sxs-lookup"><span data-stu-id="20a2e-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="20a2e-111">O comando também usa uma matriz de objetos de configuração de armazenamento armazenados $StorageAccounts variável.</span><span class="sxs-lookup"><span data-stu-id="20a2e-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="20a2e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="20a2e-112">PARAMETERS</span></span>

### <span data-ttu-id="20a2e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="20a2e-113">-AccountName</span></span>
<span data-ttu-id="20a2e-114">Especifica o nome do serviço de mídia que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="20a2e-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a2e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a2e-115">-DefaultProfile</span></span>
<span data-ttu-id="20a2e-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="20a2e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a2e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20a2e-117">-ResourceGroupName</span></span>
<span data-ttu-id="20a2e-118">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="20a2e-118">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a2e-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="20a2e-119">-StorageAccounts</span></span>
<span data-ttu-id="20a2e-120">Especifica uma matriz de contas de armazenamento que esse cmdlet associa ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="20a2e-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a2e-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="20a2e-121">-Tag</span></span>
<span data-ttu-id="20a2e-122">As marcas associadas à conta de mídia.</span><span class="sxs-lookup"><span data-stu-id="20a2e-122">The tags associated with the media account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a2e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20a2e-123">-Confirm</span></span>
<span data-ttu-id="20a2e-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20a2e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a2e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20a2e-125">-WhatIf</span></span>
<span data-ttu-id="20a2e-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20a2e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20a2e-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20a2e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a2e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a2e-128">CommonParameters</span></span>
<span data-ttu-id="20a2e-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a2e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a2e-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20a2e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a2e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20a2e-131">INPUTS</span></span>

### <span data-ttu-id="20a2e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="20a2e-132">System.String</span></span>

### <span data-ttu-id="20a2e-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="20a2e-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="20a2e-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="20a2e-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="20a2e-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="20a2e-135">OUTPUTS</span></span>

### <span data-ttu-id="20a2e-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="20a2e-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="20a2e-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="20a2e-137">NOTES</span></span>

## <span data-ttu-id="20a2e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20a2e-138">RELATED LINKS</span></span>

[<span data-ttu-id="20a2e-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="20a2e-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="20a2e-140">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="20a2e-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="20a2e-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="20a2e-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


