---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: ec411d7e1afd71849ec2d490ee70eeb0283303ca
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402381"
---
# <span data-ttu-id="2a48f-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="2a48f-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="2a48f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a48f-102">SYNOPSIS</span></span>
<span data-ttu-id="2a48f-103">Crie uma configuração de conta de armazenamento para os cmdlets do serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="2a48f-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="2a48f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a48f-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a48f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a48f-105">DESCRIPTION</span></span>
<span data-ttu-id="2a48f-106">O cmdlet **New-AzMediaServiceStorageConfig** cria uma configuração de conta de armazenamento para os cmdlets do serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="2a48f-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="2a48f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2a48f-107">EXAMPLES</span></span>

### <span data-ttu-id="2a48f-108">Exemplo 1: Criar uma configuração de conta de armazenamento para os cmdlets do serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="2a48f-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="2a48f-109">O primeiro comando cria um objeto de conta de armazenamento usando o cmdlet **New-AzStorageAccount.**</span><span class="sxs-lookup"><span data-stu-id="2a48f-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="2a48f-110">O comando nomeia essa conta de armazenamento como Armazenamento1 e o tipo é denominado Standard_GRS e armazena o resultado na variável chamada $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="2a48f-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="2a48f-111">O segundo comando cria um objeto de configuração de armazenamento como a conta de armazenamento principal associada ao serviço de mídia usando as informações de ID da conta de armazenamento armazenadas na variável $StorageAccount armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2a48f-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="2a48f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a48f-112">PARAMETERS</span></span>

### <span data-ttu-id="2a48f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a48f-113">-DefaultProfile</span></span>
<span data-ttu-id="2a48f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2a48f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a48f-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="2a48f-115">-IsPrimary</span></span>
<span data-ttu-id="2a48f-116">Indica que o cmdlet cria a conta de armazenamento como o armazenamento principal do serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="2a48f-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

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

### <span data-ttu-id="2a48f-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2a48f-117">-StorageAccountId</span></span>
<span data-ttu-id="2a48f-118">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2a48f-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="2a48f-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2a48f-119">-Confirm</span></span>
<span data-ttu-id="2a48f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a48f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a48f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a48f-121">-WhatIf</span></span>
<span data-ttu-id="2a48f-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2a48f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a48f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2a48f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a48f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a48f-124">CommonParameters</span></span>
<span data-ttu-id="2a48f-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a48f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a48f-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a48f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a48f-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="2a48f-127">INPUTS</span></span>

### <span data-ttu-id="2a48f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2a48f-128">System.String</span></span>

## <span data-ttu-id="2a48f-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="2a48f-129">OUTPUTS</span></span>

### <span data-ttu-id="2a48f-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2a48f-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="2a48f-131">Notas</span><span class="sxs-lookup"><span data-stu-id="2a48f-131">NOTES</span></span>

## <span data-ttu-id="2a48f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a48f-132">RELATED LINKS</span></span>



