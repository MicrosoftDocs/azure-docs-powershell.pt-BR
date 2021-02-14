---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117309"
---
# <span data-ttu-id="b2d71-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="b2d71-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="b2d71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2d71-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d71-103">Verifica se um nome de domínio na cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="b2d71-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="b2d71-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2d71-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2d71-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2d71-105">DESCRIPTION</span></span>
<span data-ttu-id="b2d71-106">Verifica se um nome de domínio na cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="b2d71-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="b2d71-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b2d71-107">EXAMPLES</span></span>

### <span data-ttu-id="b2d71-108">Exemplo 1: verifique se contoso.westus.cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="b2d71-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="b2d71-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2d71-109">PARAMETERS</span></span>

### <span data-ttu-id="b2d71-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d71-110">-DefaultProfile</span></span>
<span data-ttu-id="b2d71-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b2d71-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2d71-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="b2d71-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="b2d71-113">-Local</span><span class="sxs-lookup"><span data-stu-id="b2d71-113">-Location</span></span>
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

### <span data-ttu-id="b2d71-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d71-114">CommonParameters</span></span>
<span data-ttu-id="b2d71-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2d71-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d71-116">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2d71-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d71-117">Entradas</span><span class="sxs-lookup"><span data-stu-id="b2d71-117">INPUTS</span></span>

### <span data-ttu-id="b2d71-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b2d71-118">None</span></span>

## <span data-ttu-id="b2d71-119">Saídas</span><span class="sxs-lookup"><span data-stu-id="b2d71-119">OUTPUTS</span></span>

### <span data-ttu-id="b2d71-120">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b2d71-120">System.Boolean</span></span>

## <span data-ttu-id="b2d71-121">Notas</span><span class="sxs-lookup"><span data-stu-id="b2d71-121">NOTES</span></span>

## <span data-ttu-id="b2d71-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2d71-122">RELATED LINKS</span></span>
