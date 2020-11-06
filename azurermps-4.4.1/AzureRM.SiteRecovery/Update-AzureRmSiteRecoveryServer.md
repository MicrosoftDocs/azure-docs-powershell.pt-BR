---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: AD76C752-2070-449D-BF4F-B4260B05AB02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 6afb5be21f1000cf2e18cd8a4b9e1dfa4f159ee0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432535"
---
# <span data-ttu-id="ce6e9-101">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="ce6e9-101">Update-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="ce6e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce6e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ce6e9-103">Atualiza um servidor de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="ce6e9-103">Refreshes a Site Recovery server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce6e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce6e9-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServer -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce6e9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce6e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ce6e9-106">O cmdlet **Update-AzureRmSiteRecoveryServer** atualiza um servidor do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ce6e9-106">The **Update-AzureRmSiteRecoveryServer** cmdlet refreshes an Azure Site Recovery server.</span></span>

## <span data-ttu-id="ce6e9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce6e9-107">EXAMPLES</span></span>

## <span data-ttu-id="ce6e9-108">OS</span><span class="sxs-lookup"><span data-stu-id="ce6e9-108">PARAMETERS</span></span>

### <span data-ttu-id="ce6e9-109">-Servidor</span><span class="sxs-lookup"><span data-stu-id="ce6e9-109">-Server</span></span>
<span data-ttu-id="ce6e9-110">Especifica o servidor de recuperação de site em que este cmdlet é atualizado.</span><span class="sxs-lookup"><span data-stu-id="ce6e9-110">Specifies the Site Recovery server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce6e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce6e9-111">-DefaultProfile</span></span>
<span data-ttu-id="ce6e9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce6e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6e9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce6e9-113">CommonParameters</span></span>
<span data-ttu-id="ce6e9-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce6e9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce6e9-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce6e9-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce6e9-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce6e9-116">INPUTS</span></span>

### <span data-ttu-id="ce6e9-117">ASRServer</span><span class="sxs-lookup"><span data-stu-id="ce6e9-117">ASRServer</span></span>
<span data-ttu-id="ce6e9-118">O parâmetro ' Server ' aceita o valor do tipo ' ASRServer ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="ce6e9-118">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="ce6e9-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce6e9-119">OUTPUTS</span></span>

## <span data-ttu-id="ce6e9-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce6e9-120">NOTES</span></span>

## <span data-ttu-id="ce6e9-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce6e9-121">RELATED LINKS</span></span>

[<span data-ttu-id="ce6e9-122">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="ce6e9-122">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="ce6e9-123">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="ce6e9-123">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
