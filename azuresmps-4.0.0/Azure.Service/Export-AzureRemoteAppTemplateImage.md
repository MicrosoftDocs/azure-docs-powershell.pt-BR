---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D35C580F-437A-40F9-B6BA-412A1176292A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9821602df196604100de5926a7d9510bdb011bd2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945681"
---
# <span data-ttu-id="728db-101">Export-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="728db-101">Export-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="728db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="728db-102">SYNOPSIS</span></span>
<span data-ttu-id="728db-103">Exporta a imagem de modelo de uma coleção do Azure RemoteApp para a conta de armazenamento do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="728db-103">Exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="728db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="728db-104">SYNTAX</span></span>

```
Export-AzureRemoteAppTemplateImage [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingTemplateImage] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="728db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="728db-105">DESCRIPTION</span></span>
<span data-ttu-id="728db-106">O cmdlet **Export-AzureRemoteAppTemplateImage** exporta a imagem de modelo de uma coleção do Azure RemoteApp para a conta de armazenamento do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="728db-106">The **Export-AzureRemoteAppTemplateImage** cmdlet exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="728db-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="728db-107">EXAMPLES</span></span>

### <span data-ttu-id="728db-108">Exemplo 1: exportar uma imagem de modelo para a conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="728db-108">Example 1: Export a template image to the Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppTemplateImage -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingTemplateImage
```

<span data-ttu-id="728db-109">Esse comando exporta a imagem de modelo da coleção chamada contoso para um contêiner chamado ContainerName na conta de armazenamento do Azure especificada com o nome AccountName e a chave AccountKey.</span><span class="sxs-lookup"><span data-stu-id="728db-109">This command exports the template image of the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="728db-110">OS</span><span class="sxs-lookup"><span data-stu-id="728db-110">PARAMETERS</span></span>

### <span data-ttu-id="728db-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="728db-111">-CollectionName</span></span>
<span data-ttu-id="728db-112">Especifica o nome da coleção do Azure RemoteApp de origem.</span><span class="sxs-lookup"><span data-stu-id="728db-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="728db-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="728db-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="728db-114">Especifica o nome de um contêiner na conta de armazenamento do Azure de destino.</span><span class="sxs-lookup"><span data-stu-id="728db-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="728db-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="728db-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="728db-116">Especifica a chave da conta de armazenamento do Azure de destino.</span><span class="sxs-lookup"><span data-stu-id="728db-116">Specifies the key of the destination Azure storage account.</span></span>

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

### <span data-ttu-id="728db-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="728db-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="728db-118">Especifica o nome da conta de armazenamento do Azure de destino.</span><span class="sxs-lookup"><span data-stu-id="728db-118">Specifies the name of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="728db-119">-OverwriteExistingTemplateImage</span><span class="sxs-lookup"><span data-stu-id="728db-119">-OverwriteExistingTemplateImage</span></span>
<span data-ttu-id="728db-120">Indica que o cmdlet substitui a imagem de modelo existente.</span><span class="sxs-lookup"><span data-stu-id="728db-120">Indicates that the cmdlet overwrites the existing template image.</span></span>

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

### <span data-ttu-id="728db-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="728db-121">-Profile</span></span>
<span data-ttu-id="728db-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="728db-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="728db-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="728db-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="728db-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="728db-124">-Confirm</span></span>
<span data-ttu-id="728db-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="728db-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="728db-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="728db-126">-WhatIf</span></span>
<span data-ttu-id="728db-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="728db-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="728db-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="728db-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="728db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728db-129">CommonParameters</span></span>
<span data-ttu-id="728db-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="728db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728db-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="728db-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728db-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="728db-132">INPUTS</span></span>

## <span data-ttu-id="728db-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="728db-133">OUTPUTS</span></span>

## <span data-ttu-id="728db-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="728db-134">NOTES</span></span>

## <span data-ttu-id="728db-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="728db-135">RELATED LINKS</span></span>

[<span data-ttu-id="728db-136">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="728db-136">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="728db-137">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="728db-137">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="728db-138">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="728db-138">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="728db-139">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="728db-139">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


