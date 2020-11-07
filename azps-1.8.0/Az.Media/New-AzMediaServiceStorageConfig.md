---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: 8fb6e4a683decc8b5615a7cf0c8088681578f8ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770372"
---
# <span data-ttu-id="11b0e-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="11b0e-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="11b0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="11b0e-103">Crie uma configuração de conta de armazenamento para os cmdlets do serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="11b0e-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="11b0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11b0e-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11b0e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11b0e-105">DESCRIPTION</span></span>
<span data-ttu-id="11b0e-106">O cmdlet **New-AzMediaServiceStorageConfig** cria uma configuração de conta de armazenamento para os cmdlets do serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="11b0e-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="11b0e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11b0e-107">EXAMPLES</span></span>

### <span data-ttu-id="11b0e-108">Exemplo 1: criar uma configuração de conta de armazenamento para os cmdlets do serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="11b0e-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="11b0e-109">O primeiro comando cria um objeto de conta de armazenamento usando **o cmdlet New-AzStorageAccount** .</span><span class="sxs-lookup"><span data-stu-id="11b0e-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="11b0e-110">Os nomes de comando que a conta de armazenamento Storage1 e o tipo são nomeados Standard_GRS e armazena o resultado na variável chamada $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="11b0e-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="11b0e-111">O segundo comando cria um objeto de configuração de armazenamento como a conta de armazenamento principal associada ao serviço de mídia usando as informações de ID da conta de armazenamento armazenadas na variável $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="11b0e-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="11b0e-112">OS</span><span class="sxs-lookup"><span data-stu-id="11b0e-112">PARAMETERS</span></span>

### <span data-ttu-id="11b0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b0e-113">-DefaultProfile</span></span>
<span data-ttu-id="11b0e-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="11b0e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11b0e-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="11b0e-115">-IsPrimary</span></span>
<span data-ttu-id="11b0e-116">Indica que o cmdlet cria a conta de armazenamento como o armazenamento principal para o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="11b0e-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

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

### <span data-ttu-id="11b0e-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="11b0e-117">-StorageAccountId</span></span>
<span data-ttu-id="11b0e-118">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="11b0e-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="11b0e-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="11b0e-119">-Confirm</span></span>
<span data-ttu-id="11b0e-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11b0e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11b0e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b0e-121">-WhatIf</span></span>
<span data-ttu-id="11b0e-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11b0e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11b0e-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11b0e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11b0e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b0e-124">CommonParameters</span></span>
<span data-ttu-id="11b0e-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11b0e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b0e-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b0e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b0e-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11b0e-127">INPUTS</span></span>

### <span data-ttu-id="11b0e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="11b0e-128">System.String</span></span>

## <span data-ttu-id="11b0e-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11b0e-129">OUTPUTS</span></span>

### <span data-ttu-id="11b0e-130">Microsoft. Azure. Commands. Media. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11b0e-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="11b0e-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11b0e-131">NOTES</span></span>

## <span data-ttu-id="11b0e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11b0e-132">RELATED LINKS</span></span>

[<span data-ttu-id="11b0e-133">Sync-AzMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="11b0e-133">Sync-AzMediaServiceStorageKeys</span></span>](./Sync-AzMediaServiceStorageKeys.md)


