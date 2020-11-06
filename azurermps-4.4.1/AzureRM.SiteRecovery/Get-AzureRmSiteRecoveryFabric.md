---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 591cbcbc4663bde7b9d6e9bd4e35a1e91728cd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429082"
---
# <span data-ttu-id="4d0b9-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="4d0b9-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="4d0b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="4d0b9-103">Obter as propriedades de uma malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4d0b9-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d0b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d0b9-104">SYNTAX</span></span>

### <span data-ttu-id="4d0b9-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="4d0b9-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d0b9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4d0b9-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d0b9-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4d0b9-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d0b9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d0b9-108">DESCRIPTION</span></span>
<span data-ttu-id="4d0b9-109">O cmdlet **Get-AzureRmSiteRecoveryFabric** Obtém as propriedades de uma malha de recuperação de site do Azure especificada ou todas as malhas do Azure site Recovery em um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4d0b9-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="4d0b9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d0b9-110">EXAMPLES</span></span>

## <span data-ttu-id="4d0b9-111">OS</span><span class="sxs-lookup"><span data-stu-id="4d0b9-111">PARAMETERS</span></span>

### <span data-ttu-id="4d0b9-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4d0b9-112">-FriendlyName</span></span>
<span data-ttu-id="4d0b9-113">Especifica o nome amigável da malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4d0b9-113">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="4d0b9-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d0b9-114">-Name</span></span>
<span data-ttu-id="4d0b9-115">Especifica o nome da malha de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d0b9-115">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="4d0b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d0b9-116">-DefaultProfile</span></span>
<span data-ttu-id="4d0b9-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d0b9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d0b9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d0b9-118">CommonParameters</span></span>
<span data-ttu-id="4d0b9-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d0b9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d0b9-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d0b9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d0b9-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d0b9-121">INPUTS</span></span>

## <span data-ttu-id="4d0b9-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d0b9-122">OUTPUTS</span></span>

### <span data-ttu-id="4d0b9-123">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4d0b9-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4d0b9-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d0b9-124">NOTES</span></span>

## <span data-ttu-id="4d0b9-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d0b9-125">RELATED LINKS</span></span>

[<span data-ttu-id="4d0b9-126">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="4d0b9-126">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="4d0b9-127">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="4d0b9-127">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
