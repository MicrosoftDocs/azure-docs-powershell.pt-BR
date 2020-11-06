---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 63d28696370f5219a4c2a21c6fb3097441a11433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431592"
---
# <span data-ttu-id="43c61-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="43c61-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="43c61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43c61-102">SYNOPSIS</span></span>
<span data-ttu-id="43c61-103">Obter as propriedades de uma malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="43c61-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43c61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43c61-104">SYNTAX</span></span>

### <span data-ttu-id="43c61-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="43c61-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43c61-106">ByName</span><span class="sxs-lookup"><span data-stu-id="43c61-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43c61-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="43c61-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43c61-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43c61-108">DESCRIPTION</span></span>
<span data-ttu-id="43c61-109">O cmdlet **Get-AzureRmSiteRecoveryFabric** Obtém as propriedades de uma malha de recuperação de site do Azure especificada ou todas as malhas do Azure site Recovery em um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="43c61-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="43c61-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43c61-110">EXAMPLES</span></span>

## <span data-ttu-id="43c61-111">OS</span><span class="sxs-lookup"><span data-stu-id="43c61-111">PARAMETERS</span></span>

### <span data-ttu-id="43c61-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c61-112">-DefaultProfile</span></span>
<span data-ttu-id="43c61-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43c61-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c61-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="43c61-114">-FriendlyName</span></span>
<span data-ttu-id="43c61-115">Especifica o nome amigável da malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="43c61-115">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c61-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="43c61-116">-Name</span></span>
<span data-ttu-id="43c61-117">Especifica o nome da malha de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="43c61-117">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c61-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c61-118">CommonParameters</span></span>
<span data-ttu-id="43c61-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c61-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c61-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43c61-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c61-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43c61-121">INPUTS</span></span>

### <span data-ttu-id="43c61-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="43c61-122">None</span></span>
<span data-ttu-id="43c61-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="43c61-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43c61-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43c61-124">OUTPUTS</span></span>

### <span data-ttu-id="43c61-125">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="43c61-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="43c61-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43c61-126">NOTES</span></span>

## <span data-ttu-id="43c61-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43c61-127">RELATED LINKS</span></span>

[<span data-ttu-id="43c61-128">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="43c61-128">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="43c61-129">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="43c61-129">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
