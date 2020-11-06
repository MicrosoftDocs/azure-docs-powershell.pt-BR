---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 5b269eef98072a7daaaf21aa0160167bb714c77a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598681"
---
# <span data-ttu-id="94f7e-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="94f7e-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="94f7e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="94f7e-103">Obter a propriedade NetWorkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="94f7e-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="94f7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94f7e-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94f7e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="94f7e-106">O cmdlet **Get-AzStorageAccountNetworkRuleSet** Obtém a propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="94f7e-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="94f7e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94f7e-107">EXAMPLES</span></span>

### <span data-ttu-id="94f7e-108">Exemplo 1: obter a propriedade NetworkRule de uma conta de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="94f7e-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="94f7e-109">Este comando obtém a propriedade NetworkRule de uma conta de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="94f7e-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="94f7e-110">OS</span><span class="sxs-lookup"><span data-stu-id="94f7e-110">PARAMETERS</span></span>

### <span data-ttu-id="94f7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f7e-111">-DefaultProfile</span></span>
<span data-ttu-id="94f7e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94f7e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94f7e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="94f7e-113">-Name</span></span>
<span data-ttu-id="94f7e-114">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="94f7e-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="94f7e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f7e-115">-ResourceGroupName</span></span>
<span data-ttu-id="94f7e-116">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="94f7e-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="94f7e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f7e-117">CommonParameters</span></span>
<span data-ttu-id="94f7e-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f7e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f7e-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94f7e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f7e-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94f7e-120">INPUTS</span></span>

### <span data-ttu-id="94f7e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="94f7e-121">System.String</span></span>

## <span data-ttu-id="94f7e-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94f7e-122">OUTPUTS</span></span>

### <span data-ttu-id="94f7e-123">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="94f7e-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="94f7e-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94f7e-124">NOTES</span></span>

## <span data-ttu-id="94f7e-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94f7e-125">RELATED LINKS</span></span>
