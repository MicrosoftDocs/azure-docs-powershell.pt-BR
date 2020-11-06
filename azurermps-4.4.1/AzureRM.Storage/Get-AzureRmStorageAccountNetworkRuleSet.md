---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 00447be14fe61b76a4dbb4f62e3393bb76c1ddb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610971"
---
# <span data-ttu-id="d3833-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3833-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="d3833-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3833-102">SYNOPSIS</span></span>
<span data-ttu-id="d3833-103">Obter a propriedade NetWorkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d3833-103">Get the NetWorkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3833-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3833-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3833-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3833-105">DESCRIPTION</span></span>
<span data-ttu-id="d3833-106">O cmdlet **Get-AzureRmStorageAccountNetworkRuleSet** Obtém a propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d3833-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="d3833-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3833-107">EXAMPLES</span></span>

### <span data-ttu-id="d3833-108">Exemplo 1: obter a propriedade NetworkRule de uma conta de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="d3833-108">Example 1: Get NetworkRule property of a specified storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="d3833-109">Este comando obtém a propriedade NetworkRule de uma conta de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="d3833-109">This command gets NetworkRule property of a specified storage account</span></span>

## <span data-ttu-id="d3833-110">OS</span><span class="sxs-lookup"><span data-stu-id="d3833-110">PARAMETERS</span></span>

### <span data-ttu-id="d3833-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3833-111">-Name</span></span>
<span data-ttu-id="d3833-112">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d3833-112">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="d3833-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3833-113">-ResourceGroupName</span></span>
<span data-ttu-id="d3833-114">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d3833-114">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="d3833-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3833-115">-DefaultProfile</span></span>
<span data-ttu-id="d3833-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3833-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3833-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3833-117">CommonParameters</span></span>
<span data-ttu-id="d3833-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3833-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3833-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3833-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3833-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3833-120">INPUTS</span></span>

### <span data-ttu-id="d3833-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d3833-121">System.String</span></span>

## <span data-ttu-id="d3833-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3833-122">OUTPUTS</span></span>

### <span data-ttu-id="d3833-123">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3833-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="d3833-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3833-124">NOTES</span></span>

## <span data-ttu-id="d3833-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3833-125">RELATED LINKS</span></span>

