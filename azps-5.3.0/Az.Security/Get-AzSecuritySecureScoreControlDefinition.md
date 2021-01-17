---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433268"
---
# <span data-ttu-id="24e33-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="24e33-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="24e33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24e33-102">SYNOPSIS</span></span>
<span data-ttu-id="24e33-103">Obtém definições de controle de Pontuação segura de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="24e33-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="24e33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24e33-104">SYNTAX</span></span>

### <span data-ttu-id="24e33-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="24e33-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24e33-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="24e33-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24e33-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24e33-107">EXAMPLES</span></span>

### <span data-ttu-id="24e33-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="24e33-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="24e33-109">Obtém todas as definições de controle de Pontuação segura de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="24e33-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="24e33-110">OS</span><span class="sxs-lookup"><span data-stu-id="24e33-110">PARAMETERS</span></span>

### <span data-ttu-id="24e33-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e33-111">-DefaultProfile</span></span>
<span data-ttu-id="24e33-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24e33-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e33-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e33-113">CommonParameters</span></span>
<span data-ttu-id="24e33-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24e33-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e33-115">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24e33-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e33-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24e33-116">INPUTS</span></span>

### <span data-ttu-id="24e33-117">System. String</span><span class="sxs-lookup"><span data-stu-id="24e33-117">System.String</span></span>

## <span data-ttu-id="24e33-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24e33-118">OUTPUTS</span></span>

### <span data-ttu-id="24e33-119">Microsoft. Azure. Commands. Security. Models. Assessments. PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="24e33-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="24e33-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24e33-120">NOTES</span></span>

## <span data-ttu-id="24e33-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24e33-121">RELATED LINKS</span></span>
