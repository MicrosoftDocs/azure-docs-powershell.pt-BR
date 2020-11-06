---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: 9c512c1993700e1bbdab4d5c0d52a1aa2ceeafb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440711"
---
# <span data-ttu-id="f3142-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f3142-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="f3142-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3142-102">SYNOPSIS</span></span>
<span data-ttu-id="f3142-103">Remove uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f3142-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3142-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3142-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3142-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3142-105">DESCRIPTION</span></span>
<span data-ttu-id="f3142-106">O cmdlet **Remove-AzureRmStorageAccount** remove uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f3142-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="f3142-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3142-107">EXAMPLES</span></span>

### <span data-ttu-id="f3142-108">Exemplo 1: remover uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f3142-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="f3142-109">Este comando Remove a conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="f3142-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="f3142-110">OS</span><span class="sxs-lookup"><span data-stu-id="f3142-110">PARAMETERS</span></span>

### <span data-ttu-id="f3142-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3142-111">-AsJob</span></span>
<span data-ttu-id="f3142-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f3142-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3142-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3142-113">-DefaultProfile</span></span>
<span data-ttu-id="f3142-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3142-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3142-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f3142-115">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3142-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3142-116">-Name</span></span>
<span data-ttu-id="f3142-117">Especifica o nome da conta de armazenamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f3142-117">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3142-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3142-118">-ResourceGroupName</span></span>
<span data-ttu-id="f3142-119">Especifica o nome do grupo de recursos que contém a conta de armazenamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f3142-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="f3142-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f3142-120">-Confirm</span></span>
<span data-ttu-id="f3142-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3142-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3142-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3142-122">-WhatIf</span></span>
<span data-ttu-id="f3142-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f3142-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3142-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3142-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3142-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3142-125">CommonParameters</span></span>
<span data-ttu-id="f3142-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3142-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3142-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3142-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3142-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3142-128">INPUTS</span></span>

### <span data-ttu-id="f3142-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f3142-129">System.String</span></span>

## <span data-ttu-id="f3142-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3142-130">OUTPUTS</span></span>

### <span data-ttu-id="f3142-131">System. void</span><span class="sxs-lookup"><span data-stu-id="f3142-131">System.Void</span></span>

## <span data-ttu-id="f3142-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3142-132">NOTES</span></span>

## <span data-ttu-id="f3142-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3142-133">RELATED LINKS</span></span>

[<span data-ttu-id="f3142-134">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f3142-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="f3142-135">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f3142-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="f3142-136">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f3142-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


