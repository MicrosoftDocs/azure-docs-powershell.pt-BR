---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 6d6626164000957ffaa987a71131987f35a977c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772702"
---
# <span data-ttu-id="119b2-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="119b2-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="119b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="119b2-102">SYNOPSIS</span></span>
<span data-ttu-id="119b2-103">Verifica se um nome de domínio na zona cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="119b2-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="119b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="119b2-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="119b2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="119b2-105">DESCRIPTION</span></span>
<span data-ttu-id="119b2-106">Verifica se um nome de domínio na zona cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="119b2-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="119b2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="119b2-107">EXAMPLES</span></span>

### <span data-ttu-id="119b2-108">Exemplo 1: verificar se o contoso.cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="119b2-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="119b2-109">OS</span><span class="sxs-lookup"><span data-stu-id="119b2-109">PARAMETERS</span></span>

### <span data-ttu-id="119b2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="119b2-110">-DefaultProfile</span></span>
<span data-ttu-id="119b2-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="119b2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="119b2-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="119b2-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="119b2-113">-Local</span><span class="sxs-lookup"><span data-stu-id="119b2-113">-Location</span></span>
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

### <span data-ttu-id="119b2-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="119b2-114">CommonParameters</span></span>
<span data-ttu-id="119b2-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="119b2-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="119b2-116">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="119b2-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="119b2-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="119b2-117">INPUTS</span></span>

### <span data-ttu-id="119b2-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="119b2-118">None</span></span>

## <span data-ttu-id="119b2-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="119b2-119">OUTPUTS</span></span>

### <span data-ttu-id="119b2-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="119b2-120">System.Boolean</span></span>

## <span data-ttu-id="119b2-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="119b2-121">NOTES</span></span>

## <span data-ttu-id="119b2-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="119b2-122">RELATED LINKS</span></span>