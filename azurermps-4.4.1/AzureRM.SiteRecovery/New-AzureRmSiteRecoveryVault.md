---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 786e3c17ca64acf908d06b88462f44af502e36c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602684"
---
# <span data-ttu-id="6bcd5-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="6bcd5-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="6bcd5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6bcd5-102">SYNOPSIS</span></span>
<span data-ttu-id="6bcd5-103">Cria um cofre de serviços de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="6bcd5-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bcd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bcd5-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bcd5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6bcd5-105">DESCRIPTION</span></span>
<span data-ttu-id="6bcd5-106">O cmdlet **New-AzureRmSiteRecoveryVault** cria um cofre de serviços de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="6bcd5-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="6bcd5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6bcd5-107">EXAMPLES</span></span>

## <span data-ttu-id="6bcd5-108">OS</span><span class="sxs-lookup"><span data-stu-id="6bcd5-108">PARAMETERS</span></span>

### <span data-ttu-id="6bcd5-109">-Local</span><span class="sxs-lookup"><span data-stu-id="6bcd5-109">-Location</span></span>
<span data-ttu-id="6bcd5-110">Especifica o nome da localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="6bcd5-110">Specifies the geographical location name.</span></span>

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

### <span data-ttu-id="6bcd5-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="6bcd5-111">-Name</span></span>
<span data-ttu-id="6bcd5-112">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="6bcd5-112">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="6bcd5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bcd5-113">-ResourceGroupName</span></span>
<span data-ttu-id="6bcd5-114">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6bcd5-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6bcd5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bcd5-115">-DefaultProfile</span></span>
<span data-ttu-id="6bcd5-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6bcd5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bcd5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bcd5-117">CommonParameters</span></span>
<span data-ttu-id="6bcd5-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bcd5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bcd5-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bcd5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bcd5-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6bcd5-120">INPUTS</span></span>

## <span data-ttu-id="6bcd5-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6bcd5-121">OUTPUTS</span></span>

## <span data-ttu-id="6bcd5-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6bcd5-122">NOTES</span></span>

## <span data-ttu-id="6bcd5-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6bcd5-123">RELATED LINKS</span></span>

[<span data-ttu-id="6bcd5-124">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="6bcd5-124">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="6bcd5-125">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="6bcd5-125">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
