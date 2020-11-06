---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 396243e366f6a21e2ac94d105473b348c6a8198d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432742"
---
# <span data-ttu-id="9a47e-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="9a47e-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="9a47e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a47e-102">SYNOPSIS</span></span>
<span data-ttu-id="9a47e-103">Verifica a disponibilidade do nome do NameSpace especificado</span><span class="sxs-lookup"><span data-stu-id="9a47e-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a47e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a47e-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a47e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a47e-105">DESCRIPTION</span></span>
<span data-ttu-id="9a47e-106">O cmdlet **Test-AzureRmRelayName** verifica a disponibilidade do nome do namespace</span><span class="sxs-lookup"><span data-stu-id="9a47e-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="9a47e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a47e-107">EXAMPLES</span></span>

### <span data-ttu-id="9a47e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9a47e-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="9a47e-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9a47e-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="9a47e-110">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9a47e-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="9a47e-111">Retorna o status na disponibilidade do nome do namespace</span><span class="sxs-lookup"><span data-stu-id="9a47e-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="9a47e-112">OS</span><span class="sxs-lookup"><span data-stu-id="9a47e-112">PARAMETERS</span></span>

### <span data-ttu-id="9a47e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a47e-113">-DefaultProfile</span></span>
<span data-ttu-id="9a47e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a47e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a47e-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9a47e-115">-Namespace</span></span>
<span data-ttu-id="9a47e-116">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="9a47e-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="9a47e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a47e-117">CommonParameters</span></span>
<span data-ttu-id="9a47e-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a47e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9a47e-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a47e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a47e-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a47e-120">INPUTS</span></span>

### <span data-ttu-id="9a47e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9a47e-121">System.String</span></span>


## <span data-ttu-id="9a47e-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a47e-122">OUTPUTS</span></span>

### <span data-ttu-id="9a47e-123">Microsoft. Azure. Commands. Relay. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="9a47e-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="9a47e-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a47e-124">NOTES</span></span>

## <span data-ttu-id="9a47e-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a47e-125">RELATED LINKS</span></span>
