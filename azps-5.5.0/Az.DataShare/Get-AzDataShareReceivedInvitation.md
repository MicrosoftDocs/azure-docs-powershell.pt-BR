---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 939b50f6725497bb28ea333f13c04c6281f34611
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116236"
---
# <span data-ttu-id="81a7c-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="81a7c-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="81a7c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="81a7c-103">Obtém informações sobre convites de consumidor.</span><span class="sxs-lookup"><span data-stu-id="81a7c-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="81a7c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81a7c-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81a7c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="81a7c-105">DESCRIPTION</span></span>
<span data-ttu-id="81a7c-106">O cmdlet **Get-AzDataSharerevitationInvitation** fornece informações sobre todos os convites que o consumidor receievou.</span><span class="sxs-lookup"><span data-stu-id="81a7c-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="81a7c-107">Se você fornecer o local ou a ID do convite, este cmdlet fornecerá informações sobre o convite em um local específico ou ter a ID do convite. Caso contrário, ele fornece uma lista de convites enviados para o consumidor.</span><span class="sxs-lookup"><span data-stu-id="81a7c-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="81a7c-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="81a7c-108">EXAMPLES</span></span>

### <span data-ttu-id="81a7c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="81a7c-109">Example 1</span></span>
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

<span data-ttu-id="81a7c-110">Este commant fornece informações sobre convites de consumidor.</span><span class="sxs-lookup"><span data-stu-id="81a7c-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="81a7c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81a7c-111">PARAMETERS</span></span>

### <span data-ttu-id="81a7c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a7c-112">-DefaultProfile</span></span>
<span data-ttu-id="81a7c-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81a7c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81a7c-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="81a7c-114">-InvitationId</span></span>
<span data-ttu-id="81a7c-115">ID do convite do Azure dataShare.</span><span class="sxs-lookup"><span data-stu-id="81a7c-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="81a7c-116">-Local</span><span class="sxs-lookup"><span data-stu-id="81a7c-116">-Location</span></span>
<span data-ttu-id="81a7c-117">Local do convite de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="81a7c-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="81a7c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a7c-118">CommonParameters</span></span>
<span data-ttu-id="81a7c-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a7c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a7c-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81a7c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a7c-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="81a7c-121">INPUTS</span></span>

### <span data-ttu-id="81a7c-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="81a7c-122">None</span></span>

## <span data-ttu-id="81a7c-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="81a7c-123">OUTPUTS</span></span>

### <span data-ttu-id="81a7c-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="81a7c-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="81a7c-125">Notas</span><span class="sxs-lookup"><span data-stu-id="81a7c-125">NOTES</span></span>

## <span data-ttu-id="81a7c-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81a7c-126">RELATED LINKS</span></span>
