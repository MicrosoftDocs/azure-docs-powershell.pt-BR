---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: d969dcc0906def107b68a76980b39482dfe8c4e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776197"
---
# <span data-ttu-id="e4fe2-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4fe2-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="e4fe2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="e4fe2-103">Remove uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4fe2-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="e4fe2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4fe2-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4fe2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4fe2-105">DESCRIPTION</span></span>
<span data-ttu-id="e4fe2-106">O cmdlet **Remove-AzStorageAccount** remove uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4fe2-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="e4fe2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4fe2-107">EXAMPLES</span></span>

### <span data-ttu-id="e4fe2-108">Exemplo 1: remover uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e4fe2-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="e4fe2-109">Este comando Remove a conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="e4fe2-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="e4fe2-110">OS</span><span class="sxs-lookup"><span data-stu-id="e4fe2-110">PARAMETERS</span></span>

### <span data-ttu-id="e4fe2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4fe2-111">-AsJob</span></span>
<span data-ttu-id="e4fe2-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e4fe2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4fe2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4fe2-113">-DefaultProfile</span></span>
<span data-ttu-id="e4fe2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4fe2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4fe2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e4fe2-115">-Force</span></span>
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

### <span data-ttu-id="e4fe2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4fe2-116">-Name</span></span>
<span data-ttu-id="e4fe2-117">Especifica o nome da conta de armazenamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="e4fe2-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="e4fe2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4fe2-118">-ResourceGroupName</span></span>
<span data-ttu-id="e4fe2-119">Especifica o nome do grupo de recursos que contém a conta de armazenamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="e4fe2-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="e4fe2-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4fe2-120">-Confirm</span></span>
<span data-ttu-id="e4fe2-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4fe2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4fe2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4fe2-122">-WhatIf</span></span>
<span data-ttu-id="e4fe2-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4fe2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4fe2-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4fe2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4fe2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4fe2-125">CommonParameters</span></span>
<span data-ttu-id="e4fe2-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4fe2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4fe2-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4fe2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4fe2-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4fe2-128">INPUTS</span></span>

### <span data-ttu-id="e4fe2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e4fe2-129">System.String</span></span>

## <span data-ttu-id="e4fe2-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4fe2-130">OUTPUTS</span></span>

### <span data-ttu-id="e4fe2-131">System. void</span><span class="sxs-lookup"><span data-stu-id="e4fe2-131">System.Void</span></span>

## <span data-ttu-id="e4fe2-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4fe2-132">NOTES</span></span>

## <span data-ttu-id="e4fe2-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4fe2-133">RELATED LINKS</span></span>

[<span data-ttu-id="e4fe2-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4fe2-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="e4fe2-135">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4fe2-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="e4fe2-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4fe2-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


