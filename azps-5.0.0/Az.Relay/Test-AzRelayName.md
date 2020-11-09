---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281631"
---
# <span data-ttu-id="e4387-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="e4387-101">Test-AzRelayName</span></span>

## <span data-ttu-id="e4387-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4387-102">SYNOPSIS</span></span>
<span data-ttu-id="e4387-103">Verifica a disponibilidade do nome do NameSpace especificado</span><span class="sxs-lookup"><span data-stu-id="e4387-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="e4387-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4387-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4387-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4387-105">DESCRIPTION</span></span>
<span data-ttu-id="e4387-106">O cmdlet **Test-AzRelayName** verifica a disponibilidade do nome do namespace</span><span class="sxs-lookup"><span data-stu-id="e4387-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="e4387-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4387-107">EXAMPLES</span></span>

### <span data-ttu-id="e4387-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4387-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="e4387-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e4387-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="e4387-110">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e4387-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="e4387-111">Retorna o status na disponibilidade do nome do namespace</span><span class="sxs-lookup"><span data-stu-id="e4387-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="e4387-112">OS</span><span class="sxs-lookup"><span data-stu-id="e4387-112">PARAMETERS</span></span>

### <span data-ttu-id="e4387-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4387-113">-DefaultProfile</span></span>
<span data-ttu-id="e4387-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4387-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4387-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e4387-115">-Namespace</span></span>
<span data-ttu-id="e4387-116">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="e4387-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="e4387-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4387-117">CommonParameters</span></span>
<span data-ttu-id="e4387-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4387-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4387-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4387-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4387-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4387-120">INPUTS</span></span>

### <span data-ttu-id="e4387-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e4387-121">System.String</span></span>

## <span data-ttu-id="e4387-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4387-122">OUTPUTS</span></span>

### <span data-ttu-id="e4387-123">Microsoft. Azure. Commands. Relay. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="e4387-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="e4387-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4387-124">NOTES</span></span>

## <span data-ttu-id="e4387-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4387-125">RELATED LINKS</span></span>
