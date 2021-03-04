---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: 601b0bd8ff85ac3a89b3f07c3cf6e003c8005478
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892478"
---
# <span data-ttu-id="1d33e-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="1d33e-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="1d33e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d33e-102">SYNOPSIS</span></span>
<span data-ttu-id="1d33e-103">Crie uma configuração de conta de armazenamento para os cmdlets do serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="1d33e-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="1d33e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1d33e-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d33e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1d33e-105">DESCRIPTION</span></span>
<span data-ttu-id="1d33e-106">O cmdlet **New-AzMediaServiceStorageConfig** cria uma configuração de conta de armazenamento para os cmdlets do serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="1d33e-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="1d33e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d33e-107">EXAMPLES</span></span>

### <span data-ttu-id="1d33e-108">Exemplo 1: Criar uma configuração de conta de armazenamento para os cmdlets do serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="1d33e-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="1d33e-109">O primeiro comando cria um objeto de conta de armazenamento usando o cmdlet **New-AzStorageAccount.**</span><span class="sxs-lookup"><span data-stu-id="1d33e-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="1d33e-110">O comando nomeia essa conta de armazenamento Storage1 e o tipo é chamado Standard_GRS e armazena o resultado na variável chamada $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="1d33e-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="1d33e-111">O segundo comando cria um objeto de configuração de armazenamento como a conta de armazenamento principal associada ao serviço de mídia usando as informações de ID da conta de armazenamento armazenadas na variável $StorageAccount de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1d33e-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="1d33e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1d33e-112">PARAMETERS</span></span>

### <span data-ttu-id="1d33e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d33e-113">-DefaultProfile</span></span>
<span data-ttu-id="1d33e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1d33e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d33e-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="1d33e-115">-IsPrimary</span></span>
<span data-ttu-id="1d33e-116">Indica que o cmdlet cria a conta de armazenamento como o armazenamento principal para o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="1d33e-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

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

### <span data-ttu-id="1d33e-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1d33e-117">-StorageAccountId</span></span>
<span data-ttu-id="1d33e-118">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1d33e-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="1d33e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d33e-119">-Confirm</span></span>
<span data-ttu-id="1d33e-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d33e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d33e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d33e-121">-WhatIf</span></span>
<span data-ttu-id="1d33e-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1d33e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d33e-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1d33e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d33e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d33e-124">CommonParameters</span></span>
<span data-ttu-id="1d33e-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d33e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d33e-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d33e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d33e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d33e-127">INPUTS</span></span>

### <span data-ttu-id="1d33e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1d33e-128">System.String</span></span>

## <span data-ttu-id="1d33e-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1d33e-129">OUTPUTS</span></span>

### <span data-ttu-id="1d33e-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d33e-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="1d33e-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="1d33e-131">NOTES</span></span>

## <span data-ttu-id="1d33e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d33e-132">RELATED LINKS</span></span>

[<span data-ttu-id="1d33e-133">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="1d33e-133">Sync-AzMediaServiceStorageKey</span></span>](./Sync-AzMediaServiceStorageKey.md)


