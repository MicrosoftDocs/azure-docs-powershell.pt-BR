---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: be0b0f2aa9aa45fa69b3d57051a5671a76186abc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891694"
---
# <span data-ttu-id="f02d6-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="f02d6-101">Test-AzRelayName</span></span>

## <span data-ttu-id="f02d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f02d6-102">SYNOPSIS</span></span>
<span data-ttu-id="f02d6-103">Verifica a disponibilidade do nome namespace dado</span><span class="sxs-lookup"><span data-stu-id="f02d6-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="f02d6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f02d6-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f02d6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f02d6-105">DESCRIPTION</span></span>
<span data-ttu-id="f02d6-106">O **cmdlet Test-AzRelayName** Check Availability of the NameSpace Name</span><span class="sxs-lookup"><span data-stu-id="f02d6-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="f02d6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f02d6-107">EXAMPLES</span></span>

### <span data-ttu-id="f02d6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f02d6-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="f02d6-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f02d6-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="f02d6-110">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f02d6-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="f02d6-111">Retorna o status sobre a disponibilidade do nome do namespace</span><span class="sxs-lookup"><span data-stu-id="f02d6-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="f02d6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f02d6-112">PARAMETERS</span></span>

### <span data-ttu-id="f02d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f02d6-113">-DefaultProfile</span></span>
<span data-ttu-id="f02d6-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f02d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f02d6-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f02d6-115">-Namespace</span></span>
<span data-ttu-id="f02d6-116">Nome do Namespace de Retransmissão.</span><span class="sxs-lookup"><span data-stu-id="f02d6-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="f02d6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f02d6-117">CommonParameters</span></span>
<span data-ttu-id="f02d6-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f02d6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f02d6-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f02d6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f02d6-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f02d6-120">INPUTS</span></span>

### <span data-ttu-id="f02d6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="f02d6-121">System.String</span></span>

## <span data-ttu-id="f02d6-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f02d6-122">OUTPUTS</span></span>

### <span data-ttu-id="f02d6-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="f02d6-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="f02d6-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="f02d6-124">NOTES</span></span>

## <span data-ttu-id="f02d6-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f02d6-125">RELATED LINKS</span></span>
