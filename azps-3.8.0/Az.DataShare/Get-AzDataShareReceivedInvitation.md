---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 18cd37f1e24851720299a647a30323f9379bea6a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941169"
---
# <span data-ttu-id="9fc73-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="9fc73-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="9fc73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fc73-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc73-103">Obtém informações sobre convites do consumidor.</span><span class="sxs-lookup"><span data-stu-id="9fc73-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="9fc73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fc73-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fc73-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fc73-105">DESCRIPTION</span></span>
<span data-ttu-id="9fc73-106">O cmdlet **Get-AzDataShareReceivedInvitation** fornece informações sobre todos os convites que o consumidor tem receieved.</span><span class="sxs-lookup"><span data-stu-id="9fc73-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="9fc73-107">Se você fornecer identificação de local ou de convite, esse cmdlet fornecerá informações sobre o convite em um determinado local ou com a ID do convite. Caso contrário, ele fornece uma lista de convites enviados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="9fc73-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="9fc73-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fc73-108">EXAMPLES</span></span>

### <span data-ttu-id="9fc73-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9fc73-109">Example 1</span></span>
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

<span data-ttu-id="9fc73-110">Essa comunicação fornece informações sobre convites do consumidor.</span><span class="sxs-lookup"><span data-stu-id="9fc73-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="9fc73-111">OS</span><span class="sxs-lookup"><span data-stu-id="9fc73-111">PARAMETERS</span></span>

### <span data-ttu-id="9fc73-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc73-112">-DefaultProfile</span></span>
<span data-ttu-id="9fc73-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9fc73-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fc73-114">-Conviteid</span><span class="sxs-lookup"><span data-stu-id="9fc73-114">-InvitationId</span></span>
<span data-ttu-id="9fc73-115">ID de convite do Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="9fc73-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="9fc73-116">-Local</span><span class="sxs-lookup"><span data-stu-id="9fc73-116">-Location</span></span>
<span data-ttu-id="9fc73-117">Local do convite de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="9fc73-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="9fc73-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc73-118">CommonParameters</span></span>
<span data-ttu-id="9fc73-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fc73-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc73-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fc73-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc73-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fc73-121">INPUTS</span></span>

### <span data-ttu-id="9fc73-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9fc73-122">None</span></span>

## <span data-ttu-id="9fc73-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fc73-123">OUTPUTS</span></span>

### <span data-ttu-id="9fc73-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="9fc73-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="9fc73-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fc73-125">NOTES</span></span>

## <span data-ttu-id="9fc73-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fc73-126">RELATED LINKS</span></span>
