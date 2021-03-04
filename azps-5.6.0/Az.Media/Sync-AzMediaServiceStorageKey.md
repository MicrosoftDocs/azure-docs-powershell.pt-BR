---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: 75e83c3d861bfbe579634da0ee136f564be43ba8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889258"
---
# <span data-ttu-id="a962b-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="a962b-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="a962b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a962b-102">SYNOPSIS</span></span>
<span data-ttu-id="a962b-103">Sincroniza as teclas de conta de armazenamento para uma conta de armazenamento associada ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="a962b-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="a962b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a962b-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a962b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a962b-105">DESCRIPTION</span></span>
<span data-ttu-id="a962b-106">O cmdlet **Sync-AzMediaServiceStorageKey** sincroniza chaves de conta de armazenamento para uma conta de armazenamento associada ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="a962b-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="a962b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a962b-107">EXAMPLES</span></span>

### <span data-ttu-id="a962b-108">Exemplo 1: Sincronizar chaves de conta de armazenamento para uma conta de armazenamento associada ao serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="a962b-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="a962b-109">O primeiro comando usa o cmdlet Get-AzStorageAccount para obter a conta de armazenamento chamada Storage135 que pertence a ResourceGroup001 e armazena o resultado na variável denominada $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="a962b-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="a962b-110">O segundo comando sincroniza as chaves de conta de armazenamento para o serviço de mídia chamado MediaService001 usando a propriedade **Id** contida na variável $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="a962b-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="a962b-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a962b-111">PARAMETERS</span></span>

### <span data-ttu-id="a962b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a962b-112">-AccountName</span></span>
<span data-ttu-id="a962b-113">Especifica o nome do serviço de mídia que esse cmdlet sincroniza.</span><span class="sxs-lookup"><span data-stu-id="a962b-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

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

### <span data-ttu-id="a962b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a962b-114">-DefaultProfile</span></span>
<span data-ttu-id="a962b-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a962b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a962b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a962b-116">-ResourceGroupName</span></span>
<span data-ttu-id="a962b-117">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="a962b-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="a962b-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a962b-118">-StorageAccountId</span></span>
<span data-ttu-id="a962b-119">Especifica a ID da conta de armazenamento associada à conta de serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="a962b-119">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a962b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a962b-120">-Confirm</span></span>
<span data-ttu-id="a962b-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a962b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a962b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a962b-122">-WhatIf</span></span>
<span data-ttu-id="a962b-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a962b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a962b-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a962b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a962b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a962b-125">CommonParameters</span></span>
<span data-ttu-id="a962b-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a962b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a962b-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a962b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a962b-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a962b-128">INPUTS</span></span>

### <span data-ttu-id="a962b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a962b-129">System.String</span></span>

## <span data-ttu-id="a962b-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a962b-130">OUTPUTS</span></span>

### <span data-ttu-id="a962b-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a962b-131">System.Boolean</span></span>

## <span data-ttu-id="a962b-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="a962b-132">NOTES</span></span>

## <span data-ttu-id="a962b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a962b-133">RELATED LINKS</span></span>
