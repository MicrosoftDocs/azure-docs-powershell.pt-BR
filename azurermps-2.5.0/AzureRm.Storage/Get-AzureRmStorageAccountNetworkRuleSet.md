---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
ms.openlocfilehash: 8e3aa3bd313947712ef3831b83c75bb1349adb4f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785600"
---
# <span data-ttu-id="daa3b-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa3b-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="daa3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="daa3b-102">SYNOPSIS</span></span>
<span data-ttu-id="daa3b-103">Obter a propriedade NetWorkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="daa3b-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="daa3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="daa3b-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daa3b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="daa3b-105">DESCRIPTION</span></span>
<span data-ttu-id="daa3b-106">O cmdlet **Get-AzureRmStorageAccountNetworkRuleSet** Obtém a propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="daa3b-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="daa3b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="daa3b-107">EXAMPLES</span></span>

### <span data-ttu-id="daa3b-108">Exemplo 1: obter a propriedade NetworkRule de uma conta de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="daa3b-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="daa3b-109">Este comando obtém a propriedade NetworkRule de uma conta de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="daa3b-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="daa3b-110">OS</span><span class="sxs-lookup"><span data-stu-id="daa3b-110">PARAMETERS</span></span>

### <span data-ttu-id="daa3b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa3b-111">-DefaultProfile</span></span>
<span data-ttu-id="daa3b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="daa3b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daa3b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="daa3b-113">-Name</span></span>
<span data-ttu-id="daa3b-114">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="daa3b-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="daa3b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa3b-115">-ResourceGroupName</span></span>
<span data-ttu-id="daa3b-116">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="daa3b-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="daa3b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa3b-117">CommonParameters</span></span>
<span data-ttu-id="daa3b-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daa3b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa3b-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daa3b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa3b-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="daa3b-120">INPUTS</span></span>

### <span data-ttu-id="daa3b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="daa3b-121">System.String</span></span>

## <span data-ttu-id="daa3b-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="daa3b-122">OUTPUTS</span></span>

### <span data-ttu-id="daa3b-123">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa3b-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="daa3b-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="daa3b-124">NOTES</span></span>

## <span data-ttu-id="daa3b-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daa3b-125">RELATED LINKS</span></span>
