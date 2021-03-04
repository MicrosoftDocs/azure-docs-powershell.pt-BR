---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: aeda6548526c4ad12746ce90f1a030f85a0a8d2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885234"
---
# <span data-ttu-id="ce066-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce066-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="ce066-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce066-102">SYNOPSIS</span></span>
<span data-ttu-id="ce066-103">Modifica a conta de Armazenamento atual da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="ce066-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="ce066-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ce066-104">SYNTAX</span></span>

### <span data-ttu-id="ce066-105">UsingResourceGroupAndNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="ce066-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce066-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="ce066-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce066-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ce066-107">DESCRIPTION</span></span>
<span data-ttu-id="ce066-108">O cmdlet **Set-AzCurrentStorageAccount** modifica a conta atual de Armazenamento do Azure da assinatura especificada do Azure no Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ce066-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="ce066-109">A conta de Armazenamento atual é usada como padrão quando você acessa o Armazenamento sem especificar um nome de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ce066-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="ce066-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce066-110">EXAMPLES</span></span>

### <span data-ttu-id="ce066-111">Exemplo 1: Definir a conta de Armazenamento atual</span><span class="sxs-lookup"><span data-stu-id="ce066-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="ce066-112">Este comando define a conta de Armazenamento padrão para a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="ce066-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="ce066-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ce066-113">PARAMETERS</span></span>

### <span data-ttu-id="ce066-114">-Context</span><span class="sxs-lookup"><span data-stu-id="ce066-114">-Context</span></span>
<span data-ttu-id="ce066-115">Especifica um **objeto AzureStorageContext** para a conta de Armazenamento atual.</span><span class="sxs-lookup"><span data-stu-id="ce066-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="ce066-116">Para obter um objeto de contexto de armazenamento, use o cmdlet New-AzStorageContext de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ce066-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ce066-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce066-117">-DefaultProfile</span></span>
<span data-ttu-id="ce066-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce066-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce066-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ce066-119">-Name</span></span>
<span data-ttu-id="ce066-120">Especifica o nome da conta de armazenamento que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="ce066-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ce066-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce066-121">-ResourceGroupName</span></span>
<span data-ttu-id="ce066-122">Especifica o grupo de recursos que contém a conta de armazenamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="ce066-122">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="ce066-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce066-123">CommonParameters</span></span>
<span data-ttu-id="ce066-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce066-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce066-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce066-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce066-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce066-126">INPUTS</span></span>

### <span data-ttu-id="ce066-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ce066-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="ce066-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ce066-128">System.String</span></span>

## <span data-ttu-id="ce066-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ce066-129">OUTPUTS</span></span>

### <span data-ttu-id="ce066-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ce066-130">System.String</span></span>

## <span data-ttu-id="ce066-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="ce066-131">NOTES</span></span>

## <span data-ttu-id="ce066-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce066-132">RELATED LINKS</span></span>

[<span data-ttu-id="ce066-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce066-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


