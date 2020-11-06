---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/new-azurermmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
ms.openlocfilehash: efc157e2e4395055d1af2ef80f0a9fcc98886d15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610580"
---
# <span data-ttu-id="59a12-101">New-AzureRmMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="59a12-101">New-AzureRmMediaServiceStorageConfig</span></span>

## <span data-ttu-id="59a12-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59a12-102">SYNOPSIS</span></span>
<span data-ttu-id="59a12-103">Crie uma configuração de conta de armazenamento para os cmdlets do serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="59a12-103">Create a storage account configuration for the media service cmdlets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59a12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59a12-104">SYNTAX</span></span>

```
New-AzureRmMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59a12-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59a12-105">DESCRIPTION</span></span>
<span data-ttu-id="59a12-106">O cmdlet **New-AzureRmMediaServiceStorageConfig** cria uma configuração de conta de armazenamento para os cmdlets do serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="59a12-106">The **New-AzureRmMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="59a12-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59a12-107">EXAMPLES</span></span>

### <span data-ttu-id="59a12-108">Exemplo 1: criar uma configuração de conta de armazenamento para os cmdlets do serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="59a12-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="59a12-109">O primeiro comando cria um objeto de conta de armazenamento usando **o cmdlet New-AzureRmStorageAccount** .</span><span class="sxs-lookup"><span data-stu-id="59a12-109">The first command creates a storage account object by using **the New-AzureRmStorageAccount** cmdlet.</span></span>
<span data-ttu-id="59a12-110">Os nomes de comando que a conta de armazenamento Storage1 e o tipo são nomeados Standard_GRS e armazena o resultado na variável chamada $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="59a12-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="59a12-111">O segundo comando cria um objeto de configuração de armazenamento como a conta de armazenamento principal associada ao serviço de mídia usando as informações de ID da conta de armazenamento armazenadas na variável $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="59a12-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="59a12-112">OS</span><span class="sxs-lookup"><span data-stu-id="59a12-112">PARAMETERS</span></span>

### <span data-ttu-id="59a12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a12-113">-DefaultProfile</span></span>
<span data-ttu-id="59a12-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="59a12-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59a12-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="59a12-115">-IsPrimary</span></span>
<span data-ttu-id="59a12-116">Indica que o cmdlet cria a conta de armazenamento como o armazenamento principal para o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="59a12-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="59a12-117">-StorageAccountId</span></span>
<span data-ttu-id="59a12-118">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="59a12-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="59a12-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="59a12-119">-Confirm</span></span>
<span data-ttu-id="59a12-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59a12-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59a12-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59a12-121">-WhatIf</span></span>
<span data-ttu-id="59a12-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="59a12-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59a12-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="59a12-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59a12-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a12-124">CommonParameters</span></span>
<span data-ttu-id="59a12-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a12-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a12-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59a12-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a12-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59a12-127">INPUTS</span></span>

### <span data-ttu-id="59a12-128">System. String</span><span class="sxs-lookup"><span data-stu-id="59a12-128">System.String</span></span>

## <span data-ttu-id="59a12-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59a12-129">OUTPUTS</span></span>

### <span data-ttu-id="59a12-130">Microsoft. Azure. Commands. Media. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59a12-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="59a12-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59a12-131">NOTES</span></span>

## <span data-ttu-id="59a12-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59a12-132">RELATED LINKS</span></span>

[<span data-ttu-id="59a12-133">Sync-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="59a12-133">Sync-AzureRmMediaServiceStorageKeys</span></span>](./Sync-AzureRmMediaServiceStorageKeys.md)


