---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermcurrentstorageaccount
schema: 2.0.0
ms.openlocfilehash: 134af70c3f913d0eec8310f83341de8784f30f25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785593"
---
# <span data-ttu-id="8bad1-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8bad1-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="8bad1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bad1-102">SYNOPSIS</span></span>
<span data-ttu-id="8bad1-103">Modifica a conta de armazenamento atual da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="8bad1-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bad1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bad1-104">SYNTAX</span></span>

### <span data-ttu-id="8bad1-105">UsingResourceGroupAndNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8bad1-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bad1-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="8bad1-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8bad1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8bad1-107">DESCRIPTION</span></span>
<span data-ttu-id="8bad1-108">O cmdlet **set-AzureRmCurrentStorageAccount** modifica a conta de armazenamento atual do Azure da assinatura do Azure especificada no PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="8bad1-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="8bad1-109">A conta de armazenamento atual é usada como padrão quando você acessa o armazenamento sem especificar um nome de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8bad1-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="8bad1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bad1-110">EXAMPLES</span></span>

### <span data-ttu-id="8bad1-111">Exemplo 1: definir a conta de armazenamento atual</span><span class="sxs-lookup"><span data-stu-id="8bad1-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="8bad1-112">Este comando define a conta de armazenamento padrão para a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="8bad1-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="8bad1-113">OS</span><span class="sxs-lookup"><span data-stu-id="8bad1-113">PARAMETERS</span></span>

### <span data-ttu-id="8bad1-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8bad1-114">-Context</span></span>
<span data-ttu-id="8bad1-115">Especifica um objeto **AzureStorageContext** para a conta de armazenamento atual.</span><span class="sxs-lookup"><span data-stu-id="8bad1-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="8bad1-116">Para obter um objeto de contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="8bad1-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8bad1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bad1-117">-DefaultProfile</span></span>
<span data-ttu-id="8bad1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bad1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bad1-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bad1-119">-Name</span></span>
<span data-ttu-id="8bad1-120">Especifica o nome da conta de armazenamento que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8bad1-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8bad1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bad1-121">-ResourceGroupName</span></span>
<span data-ttu-id="8bad1-122">Especifica o grupo de recursos que contém a conta de armazenamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="8bad1-122">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="8bad1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bad1-123">CommonParameters</span></span>
<span data-ttu-id="8bad1-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bad1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bad1-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bad1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bad1-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8bad1-126">INPUTS</span></span>

### <span data-ttu-id="8bad1-127">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8bad1-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="8bad1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8bad1-128">System.String</span></span>

## <span data-ttu-id="8bad1-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8bad1-129">OUTPUTS</span></span>

### <span data-ttu-id="8bad1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8bad1-130">System.String</span></span>

## <span data-ttu-id="8bad1-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8bad1-131">NOTES</span></span>

## <span data-ttu-id="8bad1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bad1-132">RELATED LINKS</span></span>

[<span data-ttu-id="8bad1-133">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8bad1-133">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


