---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 72D332BA-A30B-45B9-875C-DF9D33299E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ddfbdc7da2f398ae1db11cf87de344c4f4ed5de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945678"
---
# <span data-ttu-id="52c8d-101">Export-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="52c8d-101">Export-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="52c8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="52c8d-103">Exporta todos os discos de usuário de um conjunto do Azure RemoteApp para a conta de armazenamento do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="52c8d-103">Exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="52c8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52c8d-104">SYNTAX</span></span>

```
Export-AzureRemoteAppUserDisk [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52c8d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52c8d-105">DESCRIPTION</span></span>
<span data-ttu-id="52c8d-106">O cmdlet **Export-AzureRemoteAppUserDisk** exporta todos os discos de usuário de uma coleção do Azure RemoteApp para a conta de armazenamento do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="52c8d-106">The **Export-AzureRemoteAppUserDisk** cmdlet exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="52c8d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52c8d-107">EXAMPLES</span></span>

### <span data-ttu-id="52c8d-108">Exemplo 1: exportar todos os discos de usuário de uma coleção para a conta de armazenamento do Azure especificada</span><span class="sxs-lookup"><span data-stu-id="52c8d-108">Example 1: Export all the user disks from a collection to the specified Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppUserDisk -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingUserDisk
```

<span data-ttu-id="52c8d-109">Esse comando exporta todos os discos de usuário da coleção chamada contoso para um contêiner chamado ContainerName na conta de armazenamento do Azure especificada com o nome AccountName e a chave AccountKey.</span><span class="sxs-lookup"><span data-stu-id="52c8d-109">This command exports all the user disks from the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="52c8d-110">OS</span><span class="sxs-lookup"><span data-stu-id="52c8d-110">PARAMETERS</span></span>

### <span data-ttu-id="52c8d-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="52c8d-111">-CollectionName</span></span>
<span data-ttu-id="52c8d-112">Especifica o nome da coleção do Azure RemoteApp de origem.</span><span class="sxs-lookup"><span data-stu-id="52c8d-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="52c8d-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="52c8d-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="52c8d-114">Especifica o nome de um contêiner na conta de armazenamento do Azure de destino.</span><span class="sxs-lookup"><span data-stu-id="52c8d-114">Specifies the name of a container in the destination Azure storage account.</span></span>

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

### <span data-ttu-id="52c8d-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="52c8d-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="52c8d-116">Especifica a chave da conta de armazenamento do Azure de destino.</span><span class="sxs-lookup"><span data-stu-id="52c8d-116">Specifies the Key of the destination Azure storage account.</span></span>

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

### <span data-ttu-id="52c8d-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="52c8d-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="52c8d-118">Especifica o nome da conta de armazenamento do Azure de destino.</span><span class="sxs-lookup"><span data-stu-id="52c8d-118">Specifies the name of the destination Azure storage account.</span></span>

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

### <span data-ttu-id="52c8d-119">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="52c8d-119">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="52c8d-120">Indica que o cmdlet substitui o disco do usuário existente.</span><span class="sxs-lookup"><span data-stu-id="52c8d-120">Indicates that the cmdlet overwrites the existing user disk.</span></span>

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

### <span data-ttu-id="52c8d-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="52c8d-121">-Profile</span></span>
<span data-ttu-id="52c8d-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="52c8d-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="52c8d-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="52c8d-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52c8d-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52c8d-124">-Confirm</span></span>
<span data-ttu-id="52c8d-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52c8d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52c8d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52c8d-126">-WhatIf</span></span>
<span data-ttu-id="52c8d-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52c8d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52c8d-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52c8d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52c8d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c8d-129">CommonParameters</span></span>
<span data-ttu-id="52c8d-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52c8d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c8d-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52c8d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c8d-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52c8d-132">INPUTS</span></span>

## <span data-ttu-id="52c8d-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52c8d-133">OUTPUTS</span></span>

## <span data-ttu-id="52c8d-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52c8d-134">NOTES</span></span>

## <span data-ttu-id="52c8d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52c8d-135">RELATED LINKS</span></span>

[<span data-ttu-id="52c8d-136">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="52c8d-136">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)

[<span data-ttu-id="52c8d-137">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="52c8d-137">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


