---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 3dfa3343edc82aaaf2c51a4e18ebc413ea3023c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430185"
---
# <span data-ttu-id="a1c25-101">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="a1c25-101">Set-AzureRmMediaService</span></span>

## <span data-ttu-id="a1c25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1c25-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c25-103">Modifica as propriedades especificadas de um serviço de mídia existente.</span><span class="sxs-lookup"><span data-stu-id="a1c25-103">Modifies specified properties of an existing media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1c25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1c25-104">SYNTAX</span></span>

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1c25-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1c25-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c25-106">O cmdlet **set-AzureRmMediaService** modifica as propriedades especificadas de um serviço de mídia existente.</span><span class="sxs-lookup"><span data-stu-id="a1c25-106">The **Set-AzureRmMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="a1c25-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1c25-107">EXAMPLES</span></span>

### <span data-ttu-id="a1c25-108">Exemplo 1: modificar um serviço de mídia existente</span><span class="sxs-lookup"><span data-stu-id="a1c25-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="a1c25-109">O primeiro comando cria uma série de marcas e armazena essas marcas na variável chamada $Tags.</span><span class="sxs-lookup"><span data-stu-id="a1c25-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="a1c25-110">Este segundo comando atualiza o serviço de mídia chamado MediaService001 que pertence ao grupo de recursos chamado ResourceGroup123 com as marcas armazenadas na variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="a1c25-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="a1c25-111">O comando também usa uma matriz de objetos de configuração de armazenamento armazenados na variável $StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="a1c25-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="a1c25-112">OS</span><span class="sxs-lookup"><span data-stu-id="a1c25-112">PARAMETERS</span></span>

### <span data-ttu-id="a1c25-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a1c25-113">-AccountName</span></span>
<span data-ttu-id="a1c25-114">Especifica o nome do serviço de mídia que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a1c25-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a1c25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c25-115">-DefaultProfile</span></span>
<span data-ttu-id="a1c25-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a1c25-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c25-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1c25-117">-ResourceGroupName</span></span>
<span data-ttu-id="a1c25-118">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="a1c25-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="a1c25-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="a1c25-119">-StorageAccounts</span></span>
<span data-ttu-id="a1c25-120">Especifica uma matriz de contas de armazenamento que este cmdlet associa ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="a1c25-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="a1c25-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="a1c25-121">-Tag</span></span>
<span data-ttu-id="a1c25-122">As marcas associadas à conta de mídia.</span><span class="sxs-lookup"><span data-stu-id="a1c25-122">The tags associated with the media account.</span></span>

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

### <span data-ttu-id="a1c25-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1c25-123">-Confirm</span></span>
<span data-ttu-id="a1c25-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1c25-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1c25-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1c25-125">-WhatIf</span></span>
<span data-ttu-id="a1c25-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1c25-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1c25-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1c25-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1c25-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c25-128">CommonParameters</span></span>
<span data-ttu-id="a1c25-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c25-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c25-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c25-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c25-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1c25-131">INPUTS</span></span>

### <span data-ttu-id="a1c25-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a1c25-132">System.String</span></span>

### <span data-ttu-id="a1c25-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a1c25-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a1c25-134">Microsoft. Azure. Commands. Media. Models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="a1c25-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="a1c25-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1c25-135">OUTPUTS</span></span>

### <span data-ttu-id="a1c25-136">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="a1c25-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="a1c25-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1c25-137">NOTES</span></span>

## <span data-ttu-id="a1c25-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1c25-138">RELATED LINKS</span></span>

[<span data-ttu-id="a1c25-139">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="a1c25-139">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="a1c25-140">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="a1c25-140">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="a1c25-141">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="a1c25-141">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)


