---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ba81e987e19d6698c8ea1d9e489d353d58007aea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598686"
---
# <span data-ttu-id="5cbd4-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5cbd4-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="5cbd4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5cbd4-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbd4-103">Obtém uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5cbd4-103">Gets a Storage account.</span></span>

## <span data-ttu-id="5cbd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5cbd4-104">SYNTAX</span></span>

### <span data-ttu-id="5cbd4-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cbd4-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5cbd4-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cbd4-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5cbd4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5cbd4-107">DESCRIPTION</span></span>
<span data-ttu-id="5cbd4-108">O cmdlet **Get-AzStorageAccount** Obtém uma conta de armazenamento especificada ou todas as contas de armazenamento em um grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="5cbd4-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="5cbd4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5cbd4-109">EXAMPLES</span></span>

### <span data-ttu-id="5cbd4-110">Exemplo 1: obter uma conta de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="5cbd4-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="5cbd4-111">Este comando obtém a conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="5cbd4-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="5cbd4-112">Exemplo 2: obter todas as contas de armazenamento em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5cbd4-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="5cbd4-113">Este comando obtém todas as contas de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5cbd4-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="5cbd4-114">Exemplo 3: obter todas as contas de armazenamento na assinatura</span><span class="sxs-lookup"><span data-stu-id="5cbd4-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="5cbd4-115">Este comando obtém todas as contas de armazenamento na assinatura.</span><span class="sxs-lookup"><span data-stu-id="5cbd4-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="5cbd4-116">OS</span><span class="sxs-lookup"><span data-stu-id="5cbd4-116">PARAMETERS</span></span>

### <span data-ttu-id="5cbd4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbd4-117">-DefaultProfile</span></span>
<span data-ttu-id="5cbd4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbd4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cbd4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5cbd4-119">-Name</span></span>
<span data-ttu-id="5cbd4-120">Especifica o nome da conta de armazenamento a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="5cbd4-120">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cbd4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cbd4-121">-ResourceGroupName</span></span>
<span data-ttu-id="5cbd4-122">Especifica o nome do grupo de recursos que contém a conta de armazenamento a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="5cbd4-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cbd4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbd4-123">CommonParameters</span></span>
<span data-ttu-id="5cbd4-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbd4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbd4-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cbd4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbd4-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5cbd4-126">INPUTS</span></span>

### <span data-ttu-id="5cbd4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5cbd4-127">System.String</span></span>

## <span data-ttu-id="5cbd4-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5cbd4-128">OUTPUTS</span></span>

### <span data-ttu-id="5cbd4-129">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5cbd4-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="5cbd4-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5cbd4-130">NOTES</span></span>

## <span data-ttu-id="5cbd4-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5cbd4-131">RELATED LINKS</span></span>

[<span data-ttu-id="5cbd4-132">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5cbd4-132">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="5cbd4-133">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5cbd4-133">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="5cbd4-134">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5cbd4-134">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


