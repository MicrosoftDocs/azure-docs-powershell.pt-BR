---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 413a357d793bd72ff7d1e30cb65e56cb5bd5f3a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430443"
---
# <span data-ttu-id="dc08f-101">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="dc08f-101">Set-AzureRmMediaService</span></span>

## <span data-ttu-id="dc08f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc08f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc08f-103">Modifica as propriedades especificadas de um serviço de mídia existente.</span><span class="sxs-lookup"><span data-stu-id="dc08f-103">Modifies specified properties of an existing media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc08f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc08f-104">SYNTAX</span></span>

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc08f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc08f-105">DESCRIPTION</span></span>
<span data-ttu-id="dc08f-106">O cmdlet **set-AzureRmMediaService** modifica as propriedades especificadas de um serviço de mídia existente.</span><span class="sxs-lookup"><span data-stu-id="dc08f-106">The **Set-AzureRmMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="dc08f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc08f-107">EXAMPLES</span></span>

### <span data-ttu-id="dc08f-108">Exemplo 1: modificar um serviço de mídia existente</span><span class="sxs-lookup"><span data-stu-id="dc08f-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="dc08f-109">O primeiro comando cria uma série de marcas e armazena essas marcas na variável chamada $Tags.</span><span class="sxs-lookup"><span data-stu-id="dc08f-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>

<span data-ttu-id="dc08f-110">Este segundo comando atualiza o serviço de mídia chamado MediaService001 que pertence ao grupo de recursos chamado ResourceGroup123 com as marcas armazenadas na variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="dc08f-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="dc08f-111">O comando também usa uma matriz de objetos de configuração de armazenamento armazenados na variável $StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="dc08f-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="dc08f-112">OS</span><span class="sxs-lookup"><span data-stu-id="dc08f-112">PARAMETERS</span></span>

### <span data-ttu-id="dc08f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dc08f-113">-AccountName</span></span>
<span data-ttu-id="dc08f-114">Especifica o nome do serviço de mídia que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="dc08f-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc08f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc08f-115">-DefaultProfile</span></span>
<span data-ttu-id="dc08f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dc08f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc08f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc08f-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc08f-118">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="dc08f-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="dc08f-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="dc08f-119">-StorageAccounts</span></span>
<span data-ttu-id="dc08f-120">Especifica uma matriz de contas de armazenamento que este cmdlet associa ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="dc08f-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc08f-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="dc08f-121">-Tag</span></span>
<span data-ttu-id="dc08f-122">As marcas associadas à conta de mídia.</span><span class="sxs-lookup"><span data-stu-id="dc08f-122">The tags associated with the media account.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc08f-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dc08f-123">-Confirm</span></span>
<span data-ttu-id="dc08f-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc08f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc08f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc08f-125">-WhatIf</span></span>
<span data-ttu-id="dc08f-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc08f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc08f-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc08f-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc08f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc08f-128">CommonParameters</span></span>
<span data-ttu-id="dc08f-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc08f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc08f-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc08f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc08f-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc08f-131">INPUTS</span></span>

### <span data-ttu-id="dc08f-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dc08f-132">None</span></span>
<span data-ttu-id="dc08f-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="dc08f-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc08f-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc08f-134">OUTPUTS</span></span>

### <span data-ttu-id="dc08f-135">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="dc08f-135">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="dc08f-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc08f-136">NOTES</span></span>

## <span data-ttu-id="dc08f-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc08f-137">RELATED LINKS</span></span>

[<span data-ttu-id="dc08f-138">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="dc08f-138">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="dc08f-139">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="dc08f-139">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="dc08f-140">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="dc08f-140">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)


