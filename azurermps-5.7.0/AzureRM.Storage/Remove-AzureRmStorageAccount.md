---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: e6a6a35b5e744218c3afc6db396e875ad0acf242
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609881"
---
# <span data-ttu-id="b1a2a-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1a2a-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="b1a2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a2a-103">Remove uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a2a-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1a2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1a2a-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1a2a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1a2a-105">DESCRIPTION</span></span>
<span data-ttu-id="b1a2a-106">O cmdlet **Remove-AzureRmStorageAccount** remove uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a2a-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="b1a2a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1a2a-107">EXAMPLES</span></span>

### <span data-ttu-id="b1a2a-108">Exemplo 1: remover uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b1a2a-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="b1a2a-109">Este comando Remove a conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="b1a2a-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="b1a2a-110">OS</span><span class="sxs-lookup"><span data-stu-id="b1a2a-110">PARAMETERS</span></span>

### <span data-ttu-id="b1a2a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b1a2a-111">-Force</span></span>
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

### <span data-ttu-id="b1a2a-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1a2a-112">-Name</span></span>
<span data-ttu-id="b1a2a-113">Especifica o nome da conta de armazenamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="b1a2a-113">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a2a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a2a-114">-ResourceGroupName</span></span>
<span data-ttu-id="b1a2a-115">Especifica o nome do grupo de recursos que contém a conta de armazenamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="b1a2a-115">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="b1a2a-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b1a2a-116">-Confirm</span></span>
<span data-ttu-id="b1a2a-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1a2a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1a2a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1a2a-118">-WhatIf</span></span>
<span data-ttu-id="b1a2a-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1a2a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1a2a-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1a2a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1a2a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a2a-121">CommonParameters</span></span>
<span data-ttu-id="b1a2a-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a2a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a2a-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a2a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a2a-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1a2a-124">INPUTS</span></span>

### <span data-ttu-id="b1a2a-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b1a2a-125">None</span></span>
<span data-ttu-id="b1a2a-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b1a2a-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1a2a-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1a2a-127">OUTPUTS</span></span>

## <span data-ttu-id="b1a2a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1a2a-128">NOTES</span></span>

## <span data-ttu-id="b1a2a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1a2a-129">RELATED LINKS</span></span>

[<span data-ttu-id="b1a2a-130">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1a2a-130">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="b1a2a-131">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1a2a-131">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="b1a2a-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1a2a-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
