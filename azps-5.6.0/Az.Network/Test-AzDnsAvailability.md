---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: dbc21a337263bb0e509188d472e4ff984e22322b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885354"
---
# <span data-ttu-id="b0334-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="b0334-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="b0334-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0334-102">SYNOPSIS</span></span>
<span data-ttu-id="b0334-103">Verifica se um nome de domínio na zona cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="b0334-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="b0334-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b0334-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0334-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b0334-105">DESCRIPTION</span></span>
<span data-ttu-id="b0334-106">Verifica se um nome de domínio na zona cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="b0334-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="b0334-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0334-107">EXAMPLES</span></span>

### <span data-ttu-id="b0334-108">Exemplo 1: verifique se contoso.westus.cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="b0334-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="b0334-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b0334-109">PARAMETERS</span></span>

### <span data-ttu-id="b0334-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0334-110">-DefaultProfile</span></span>
<span data-ttu-id="b0334-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b0334-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0334-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="b0334-112">-DomainNameLabel</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainQualifiedName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0334-113">-Location</span><span class="sxs-lookup"><span data-stu-id="b0334-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0334-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0334-114">CommonParameters</span></span>
<span data-ttu-id="b0334-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0334-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0334-116">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0334-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0334-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0334-117">INPUTS</span></span>

### <span data-ttu-id="b0334-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b0334-118">None</span></span>

## <span data-ttu-id="b0334-119">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b0334-119">OUTPUTS</span></span>

### <span data-ttu-id="b0334-120">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b0334-120">System.Boolean</span></span>

## <span data-ttu-id="b0334-121">NOTES</span><span class="sxs-lookup"><span data-stu-id="b0334-121">NOTES</span></span>

## <span data-ttu-id="b0334-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0334-122">RELATED LINKS</span></span>
