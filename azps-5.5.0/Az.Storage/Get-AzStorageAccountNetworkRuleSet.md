---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: e9ce7a0ab98251b86990db5623b91b3a62a4cdcc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117049"
---
# <span data-ttu-id="ff2ba-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff2ba-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="ff2ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff2ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ff2ba-103">Obter a propriedade NetWorkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ff2ba-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="ff2ba-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff2ba-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff2ba-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff2ba-105">DESCRIPTION</span></span>
<span data-ttu-id="ff2ba-106">O cmdlet **Get-AzStorageAccountNetworkRuleSet** obtém a propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ff2ba-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="ff2ba-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ff2ba-107">EXAMPLES</span></span>

### <span data-ttu-id="ff2ba-108">Exemplo 1: Obter a propriedade NetworkRule de uma conta de Armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="ff2ba-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="ff2ba-109">Este comando obtém a propriedade NetworkRule de uma conta de Armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="ff2ba-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="ff2ba-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff2ba-110">PARAMETERS</span></span>

### <span data-ttu-id="ff2ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff2ba-111">-DefaultProfile</span></span>
<span data-ttu-id="ff2ba-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff2ba-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff2ba-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff2ba-113">-Name</span></span>
<span data-ttu-id="ff2ba-114">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ff2ba-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="ff2ba-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff2ba-115">-ResourceGroupName</span></span>
<span data-ttu-id="ff2ba-116">Especifica o nome do grupo de recursos que contém a conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ff2ba-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="ff2ba-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff2ba-117">CommonParameters</span></span>
<span data-ttu-id="ff2ba-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff2ba-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff2ba-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff2ba-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff2ba-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="ff2ba-120">INPUTS</span></span>

### <span data-ttu-id="ff2ba-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ff2ba-121">System.String</span></span>

## <span data-ttu-id="ff2ba-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="ff2ba-122">OUTPUTS</span></span>

### <span data-ttu-id="ff2ba-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff2ba-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="ff2ba-124">Notas</span><span class="sxs-lookup"><span data-stu-id="ff2ba-124">NOTES</span></span>

## <span data-ttu-id="ff2ba-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff2ba-125">RELATED LINKS</span></span>
