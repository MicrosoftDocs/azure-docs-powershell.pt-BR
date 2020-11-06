---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: 07fdf5a05f5099facabb78f35c44856545d1efe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602560"
---
# <span data-ttu-id="61342-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61342-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="61342-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61342-102">SYNOPSIS</span></span>
<span data-ttu-id="61342-103">Obtém uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="61342-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61342-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61342-104">SYNTAX</span></span>

### <span data-ttu-id="61342-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="61342-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61342-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61342-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61342-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61342-107">DESCRIPTION</span></span>
<span data-ttu-id="61342-108">O cmdlet **Get-AzureRmStorageAccount** Obtém uma conta de armazenamento especificada ou todas as contas de armazenamento em um grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="61342-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="61342-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61342-109">EXAMPLES</span></span>

### <span data-ttu-id="61342-110">Exemplo 1: obter uma conta de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="61342-110">Example 1: Get a specified storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="61342-111">Este comando obtém a conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="61342-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="61342-112">Exemplo 2: obter todas as contas de armazenamento em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="61342-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="61342-113">Este comando obtém todas as contas de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61342-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="61342-114">Exemplo 3: obter todas as contas de armazenamento na assinatura</span><span class="sxs-lookup"><span data-stu-id="61342-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="61342-115">Este comando obtém todas as contas de armazenamento na assinatura.</span><span class="sxs-lookup"><span data-stu-id="61342-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="61342-116">OS</span><span class="sxs-lookup"><span data-stu-id="61342-116">PARAMETERS</span></span>

### <span data-ttu-id="61342-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="61342-117">-Name</span></span>
<span data-ttu-id="61342-118">Especifica o nome da conta de armazenamento a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="61342-118">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="61342-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61342-119">-ResourceGroupName</span></span>
<span data-ttu-id="61342-120">Especifica o nome do grupo de recursos que contém a conta de armazenamento a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="61342-120">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="61342-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61342-121">-DefaultProfile</span></span>
<span data-ttu-id="61342-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61342-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61342-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61342-123">CommonParameters</span></span>
<span data-ttu-id="61342-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61342-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61342-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61342-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61342-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61342-126">INPUTS</span></span>

## <span data-ttu-id="61342-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61342-127">OUTPUTS</span></span>

## <span data-ttu-id="61342-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61342-128">NOTES</span></span>

## <span data-ttu-id="61342-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61342-129">RELATED LINKS</span></span>

[<span data-ttu-id="61342-130">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61342-130">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="61342-131">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61342-131">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="61342-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61342-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


