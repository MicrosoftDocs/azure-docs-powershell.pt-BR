---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
ms.openlocfilehash: 73680e82a9d898075e905d88bcc8602609a5612d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602673"
---
# <span data-ttu-id="cc08c-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cc08c-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="cc08c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc08c-102">SYNOPSIS</span></span>
<span data-ttu-id="cc08c-103">Modifica a conta de armazenamento atual da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="cc08c-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc08c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc08c-104">SYNTAX</span></span>

### <span data-ttu-id="cc08c-105">UsingResourceGroupAndNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cc08c-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc08c-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="cc08c-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc08c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc08c-107">DESCRIPTION</span></span>
<span data-ttu-id="cc08c-108">O cmdlet **set-AzureRmCurrentStorageAccount** modifica a conta de armazenamento atual do Azure da assinatura do Azure especificada no PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc08c-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="cc08c-109">A conta de armazenamento atual é usada como padrão quando você acessa o armazenamento sem especificar um nome de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cc08c-109">The current storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="cc08c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc08c-110">EXAMPLES</span></span>

### <span data-ttu-id="cc08c-111">Exemplo 1: definir a conta de armazenamento atual</span><span class="sxs-lookup"><span data-stu-id="cc08c-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="cc08c-112">Este comando define a conta de armazenamento padrão para a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="cc08c-112">This command sets the default storage account for the specified subscription.</span></span>

## <span data-ttu-id="cc08c-113">OS</span><span class="sxs-lookup"><span data-stu-id="cc08c-113">PARAMETERS</span></span>

### <span data-ttu-id="cc08c-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cc08c-114">-Context</span></span>
<span data-ttu-id="cc08c-115">Especifica um objeto **AzureStorageContext** para a conta de armazenamento atual.</span><span class="sxs-lookup"><span data-stu-id="cc08c-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="cc08c-116">Para obter um objeto de contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="cc08c-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cc08c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc08c-117">-Name</span></span>
<span data-ttu-id="cc08c-118">Especifica o nome da conta de armazenamento que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="cc08c-118">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cc08c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc08c-119">-ResourceGroupName</span></span>
<span data-ttu-id="cc08c-120">Especifica o grupo de recursos que contém a conta de armazenamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="cc08c-120">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="cc08c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc08c-121">-DefaultProfile</span></span>
<span data-ttu-id="cc08c-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc08c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc08c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc08c-123">CommonParameters</span></span>
<span data-ttu-id="cc08c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc08c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc08c-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc08c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc08c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc08c-126">INPUTS</span></span>

## <span data-ttu-id="cc08c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc08c-127">OUTPUTS</span></span>

## <span data-ttu-id="cc08c-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc08c-128">NOTES</span></span>

## <span data-ttu-id="cc08c-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc08c-129">RELATED LINKS</span></span>

[<span data-ttu-id="cc08c-130">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cc08c-130">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


