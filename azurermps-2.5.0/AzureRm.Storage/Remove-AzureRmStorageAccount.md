---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: d3e7a04f292be8e83bc28456c0510450c078a777
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786368"
---
# <span data-ttu-id="d85e6-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d85e6-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="d85e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d85e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d85e6-103">Remove uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d85e6-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d85e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d85e6-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d85e6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d85e6-105">DESCRIPTION</span></span>
<span data-ttu-id="d85e6-106">O cmdlet **Remove-AzureRmStorageAccount** remove uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d85e6-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="d85e6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d85e6-107">EXAMPLES</span></span>

### <span data-ttu-id="d85e6-108">Exemplo 1: remover uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d85e6-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="d85e6-109">Este comando Remove a conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="d85e6-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="d85e6-110">OS</span><span class="sxs-lookup"><span data-stu-id="d85e6-110">PARAMETERS</span></span>

### <span data-ttu-id="d85e6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d85e6-111">-AsJob</span></span>
<span data-ttu-id="d85e6-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d85e6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d85e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85e6-113">-DefaultProfile</span></span>
<span data-ttu-id="d85e6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d85e6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d85e6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d85e6-115">-Force</span></span>
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

### <span data-ttu-id="d85e6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d85e6-116">-Name</span></span>
<span data-ttu-id="d85e6-117">Especifica o nome da conta de armazenamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="d85e6-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="d85e6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d85e6-118">-ResourceGroupName</span></span>
<span data-ttu-id="d85e6-119">Especifica o nome do grupo de recursos que contém a conta de armazenamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="d85e6-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="d85e6-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d85e6-120">-Confirm</span></span>
<span data-ttu-id="d85e6-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d85e6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d85e6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d85e6-122">-WhatIf</span></span>
<span data-ttu-id="d85e6-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d85e6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d85e6-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d85e6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d85e6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85e6-125">CommonParameters</span></span>
<span data-ttu-id="d85e6-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d85e6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85e6-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d85e6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85e6-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d85e6-128">INPUTS</span></span>

### <span data-ttu-id="d85e6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d85e6-129">System.String</span></span>

## <span data-ttu-id="d85e6-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d85e6-130">OUTPUTS</span></span>

### <span data-ttu-id="d85e6-131">System. void</span><span class="sxs-lookup"><span data-stu-id="d85e6-131">System.Void</span></span>

## <span data-ttu-id="d85e6-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d85e6-132">NOTES</span></span>

## <span data-ttu-id="d85e6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d85e6-133">RELATED LINKS</span></span>

[<span data-ttu-id="d85e6-134">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d85e6-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="d85e6-135">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d85e6-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="d85e6-136">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d85e6-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


