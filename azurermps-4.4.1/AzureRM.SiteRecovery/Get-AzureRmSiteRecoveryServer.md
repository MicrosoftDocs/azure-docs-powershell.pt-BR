---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: aacb061772ed1b1202528ebc7b7bc95d725bb9f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610162"
---
# <span data-ttu-id="1f222-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="1f222-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="1f222-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f222-102">SYNOPSIS</span></span>
<span data-ttu-id="1f222-103">Obtém informações sobre os servidores de recuperação de site registrados no cofre atual.</span><span class="sxs-lookup"><span data-stu-id="1f222-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f222-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f222-104">SYNTAX</span></span>

### <span data-ttu-id="1f222-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="1f222-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f222-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1f222-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f222-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="1f222-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f222-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f222-108">DESCRIPTION</span></span>
<span data-ttu-id="1f222-109">O cmdlet **Get-AzureRmSiteRecoveryServer** Obtém informações sobre os servidores de recuperação de site do Azure registrados no cofre de recuperação do site atual.</span><span class="sxs-lookup"><span data-stu-id="1f222-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="1f222-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f222-110">EXAMPLES</span></span>

## <span data-ttu-id="1f222-111">OS</span><span class="sxs-lookup"><span data-stu-id="1f222-111">PARAMETERS</span></span>

### <span data-ttu-id="1f222-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1f222-112">-FriendlyName</span></span>
<span data-ttu-id="1f222-113">Especifica o nome amigável do servidor.</span><span class="sxs-lookup"><span data-stu-id="1f222-113">Specifies the friendly name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f222-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f222-114">-Name</span></span>
<span data-ttu-id="1f222-115">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="1f222-115">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f222-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f222-116">-DefaultProfile</span></span>
<span data-ttu-id="1f222-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f222-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f222-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f222-118">CommonParameters</span></span>
<span data-ttu-id="1f222-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f222-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f222-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f222-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f222-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f222-121">INPUTS</span></span>

## <span data-ttu-id="1f222-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f222-122">OUTPUTS</span></span>

### <span data-ttu-id="1f222-123">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="1f222-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="1f222-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f222-124">NOTES</span></span>

## <span data-ttu-id="1f222-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f222-125">RELATED LINKS</span></span>

[<span data-ttu-id="1f222-126">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="1f222-126">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
