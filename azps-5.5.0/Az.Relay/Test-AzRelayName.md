---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118777"
---
# <span data-ttu-id="0f5c7-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="0f5c7-101">Test-AzRelayName</span></span>

## <span data-ttu-id="0f5c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="0f5c7-103">Verifica a Disponibilidade do nome namespace determinado</span><span class="sxs-lookup"><span data-stu-id="0f5c7-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="0f5c7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f5c7-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f5c7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f5c7-105">DESCRIPTION</span></span>
<span data-ttu-id="0f5c7-106">O **Cmdlet Test-AzRelayName** Check Availability of the NameSpace NameSpace</span><span class="sxs-lookup"><span data-stu-id="0f5c7-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="0f5c7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0f5c7-107">EXAMPLES</span></span>

### <span data-ttu-id="0f5c7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f5c7-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="0f5c7-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0f5c7-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="0f5c7-110">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0f5c7-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="0f5c7-111">retorna o status sobre a disponibilidade do nome do namespace</span><span class="sxs-lookup"><span data-stu-id="0f5c7-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="0f5c7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f5c7-112">PARAMETERS</span></span>

### <span data-ttu-id="0f5c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f5c7-113">-DefaultProfile</span></span>
<span data-ttu-id="0f5c7-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f5c7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f5c7-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0f5c7-115">-Namespace</span></span>
<span data-ttu-id="0f5c7-116">Nome do Namespace de Retransmissão.</span><span class="sxs-lookup"><span data-stu-id="0f5c7-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="0f5c7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f5c7-117">CommonParameters</span></span>
<span data-ttu-id="0f5c7-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f5c7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f5c7-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f5c7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f5c7-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="0f5c7-120">INPUTS</span></span>

### <span data-ttu-id="0f5c7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="0f5c7-121">System.String</span></span>

## <span data-ttu-id="0f5c7-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="0f5c7-122">OUTPUTS</span></span>

### <span data-ttu-id="0f5c7-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="0f5c7-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="0f5c7-124">Notas</span><span class="sxs-lookup"><span data-stu-id="0f5c7-124">NOTES</span></span>

## <span data-ttu-id="0f5c7-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f5c7-125">RELATED LINKS</span></span>
