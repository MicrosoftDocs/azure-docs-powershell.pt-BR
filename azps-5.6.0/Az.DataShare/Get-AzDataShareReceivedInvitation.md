---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 563c97ec87a758668c737465ea50642324706a9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893179"
---
# <span data-ttu-id="992ce-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="992ce-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="992ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="992ce-102">SYNOPSIS</span></span>
<span data-ttu-id="992ce-103">Obtém informações sobre convites de consumidor.</span><span class="sxs-lookup"><span data-stu-id="992ce-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="992ce-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="992ce-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="992ce-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="992ce-105">DESCRIPTION</span></span>
<span data-ttu-id="992ce-106">O cmdlet **Get-AzDataShareReceivedInvitation** fornece informações sobre todos os convites que o consumidor receieved.</span><span class="sxs-lookup"><span data-stu-id="992ce-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="992ce-107">Se você fornecer a id de local ou convite, este cmdlet fornecerá informações sobre convite em local específico ou ter id de convite. Caso contrário, ele fornece uma lista de convites enviados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="992ce-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="992ce-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="992ce-108">EXAMPLES</span></span>

### <span data-ttu-id="992ce-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="992ce-109">Example 1</span></span>
```
PS C:\> Get-AzDataShareReceivedInvitation -location "westus"

DataSetCount      : 3
InvitationId      : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus  : Pending
Location          : westus
RespondedAt       :
Sender            : adsprovider@microsoft.com
SenderCompanyName : ADS Test
SentAt            : 7/8/2019 10:47:10 PM
ShareName         : AdsShare
Description       : Some description
Terms             : Some terms of use
Id                : /providers/Microsoft.DataShare/consumerInvitations/167e06ff-567f-4bc7-be0c-645a6de710f3
Name              : AdsInvitation
Type              : Microsoft.DataShare/consumerInvitations
```

<span data-ttu-id="992ce-110">Este commant fornece informações sobre convites de consumidor.</span><span class="sxs-lookup"><span data-stu-id="992ce-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="992ce-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="992ce-111">PARAMETERS</span></span>

### <span data-ttu-id="992ce-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992ce-112">-DefaultProfile</span></span>
<span data-ttu-id="992ce-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="992ce-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="992ce-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="992ce-114">-InvitationId</span></span>
<span data-ttu-id="992ce-115">ID do convite do Azure dataShare.</span><span class="sxs-lookup"><span data-stu-id="992ce-115">Azure dataShare invitation id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992ce-116">-Location</span><span class="sxs-lookup"><span data-stu-id="992ce-116">-Location</span></span>
<span data-ttu-id="992ce-117">Local do convite do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="992ce-117">Azure data share invitation location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992ce-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992ce-118">CommonParameters</span></span>
<span data-ttu-id="992ce-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="992ce-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992ce-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="992ce-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992ce-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="992ce-121">INPUTS</span></span>

### <span data-ttu-id="992ce-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="992ce-122">None</span></span>

## <span data-ttu-id="992ce-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="992ce-123">OUTPUTS</span></span>

### <span data-ttu-id="992ce-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="992ce-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="992ce-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="992ce-125">NOTES</span></span>

## <span data-ttu-id="992ce-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="992ce-126">RELATED LINKS</span></span>
