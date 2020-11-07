---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: 24c0140f4a1ba09111db0dacaa612c4a635493fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774270"
---
# <span data-ttu-id="e713d-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e713d-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="e713d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e713d-102">SYNOPSIS</span></span>
<span data-ttu-id="e713d-103">Modifica a conta de armazenamento atual da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="e713d-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="e713d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e713d-104">SYNTAX</span></span>

### <span data-ttu-id="e713d-105">UsingResourceGroupAndNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e713d-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e713d-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="e713d-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e713d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e713d-107">DESCRIPTION</span></span>
<span data-ttu-id="e713d-108">O cmdlet **set-AzCurrentStorageAccount** modifica a conta de armazenamento atual do Azure da assinatura do Azure especificada no PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="e713d-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="e713d-109">A conta de armazenamento atual é usada como padrão quando você acessa o armazenamento sem especificar um nome de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e713d-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="e713d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e713d-110">EXAMPLES</span></span>

### <span data-ttu-id="e713d-111">Exemplo 1: definir a conta de armazenamento atual</span><span class="sxs-lookup"><span data-stu-id="e713d-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="e713d-112">Este comando define a conta de armazenamento padrão para a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="e713d-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="e713d-113">OS</span><span class="sxs-lookup"><span data-stu-id="e713d-113">PARAMETERS</span></span>

### <span data-ttu-id="e713d-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e713d-114">-Context</span></span>
<span data-ttu-id="e713d-115">Especifica um objeto **AzureStorageContext** para a conta de armazenamento atual.</span><span class="sxs-lookup"><span data-stu-id="e713d-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="e713d-116">Para obter um objeto de contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e713d-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UsingStorageContext
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e713d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e713d-117">-DefaultProfile</span></span>
<span data-ttu-id="e713d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e713d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e713d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e713d-119">-Name</span></span>
<span data-ttu-id="e713d-120">Especifica o nome da conta de armazenamento que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="e713d-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e713d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e713d-121">-ResourceGroupName</span></span>
<span data-ttu-id="e713d-122">Especifica o grupo de recursos que contém a conta de armazenamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="e713d-122">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e713d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e713d-123">CommonParameters</span></span>
<span data-ttu-id="e713d-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e713d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e713d-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e713d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e713d-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e713d-126">INPUTS</span></span>

### <span data-ttu-id="e713d-127">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e713d-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="e713d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e713d-128">System.String</span></span>

## <span data-ttu-id="e713d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e713d-129">OUTPUTS</span></span>

### <span data-ttu-id="e713d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e713d-130">System.String</span></span>

## <span data-ttu-id="e713d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e713d-131">NOTES</span></span>

## <span data-ttu-id="e713d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e713d-132">RELATED LINKS</span></span>

[<span data-ttu-id="e713d-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e713d-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)

