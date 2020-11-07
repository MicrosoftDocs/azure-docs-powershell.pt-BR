---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: dafceede3c3732af423052d33ba125c4ad292d20
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785608"
---
# <span data-ttu-id="f1006-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1006-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="f1006-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1006-102">SYNOPSIS</span></span>
<span data-ttu-id="f1006-103">Obtém uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f1006-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1006-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1006-104">SYNTAX</span></span>

### <span data-ttu-id="f1006-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1006-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1006-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1006-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1006-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1006-107">DESCRIPTION</span></span>
<span data-ttu-id="f1006-108">O cmdlet **Get-AzureRmStorageAccount** Obtém uma conta de armazenamento especificada ou todas as contas de armazenamento em um grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="f1006-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="f1006-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1006-109">EXAMPLES</span></span>

### <span data-ttu-id="f1006-110">Exemplo 1: obter uma conta de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="f1006-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="f1006-111">Este comando obtém a conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="f1006-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="f1006-112">Exemplo 2: obter todas as contas de armazenamento em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f1006-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="f1006-113">Este comando obtém todas as contas de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1006-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="f1006-114">Exemplo 3: obter todas as contas de armazenamento na assinatura</span><span class="sxs-lookup"><span data-stu-id="f1006-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="f1006-115">Este comando obtém todas as contas de armazenamento na assinatura.</span><span class="sxs-lookup"><span data-stu-id="f1006-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="f1006-116">OS</span><span class="sxs-lookup"><span data-stu-id="f1006-116">PARAMETERS</span></span>

### <span data-ttu-id="f1006-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1006-117">-DefaultProfile</span></span>
<span data-ttu-id="f1006-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1006-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1006-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1006-119">-Name</span></span>
<span data-ttu-id="f1006-120">Especifica o nome da conta de armazenamento a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="f1006-120">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="f1006-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1006-121">-ResourceGroupName</span></span>
<span data-ttu-id="f1006-122">Especifica o nome do grupo de recursos que contém a conta de armazenamento a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="f1006-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="f1006-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1006-123">CommonParameters</span></span>
<span data-ttu-id="f1006-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1006-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1006-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1006-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1006-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1006-126">INPUTS</span></span>

### <span data-ttu-id="f1006-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f1006-127">System.String</span></span>

## <span data-ttu-id="f1006-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1006-128">OUTPUTS</span></span>

### <span data-ttu-id="f1006-129">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1006-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f1006-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1006-130">NOTES</span></span>

## <span data-ttu-id="f1006-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1006-131">RELATED LINKS</span></span>

[<span data-ttu-id="f1006-132">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1006-132">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="f1006-133">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1006-133">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="f1006-134">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1006-134">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


