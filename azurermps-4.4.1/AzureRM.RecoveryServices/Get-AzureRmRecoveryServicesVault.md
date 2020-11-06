---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bd9b47b54cb609a06da10488007f55d91d157b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433028"
---
# <span data-ttu-id="1dfc3-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="1dfc3-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="1dfc3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1dfc3-102">SYNOPSIS</span></span>
<span data-ttu-id="1dfc3-103">Obtém uma lista de cofres de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1dfc3-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dfc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dfc3-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dfc3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1dfc3-105">DESCRIPTION</span></span>
<span data-ttu-id="1dfc3-106">O cmdlet **Get-AzureRmRecoveryServicesVault** Obtém uma lista de cofres de serviços de recuperação na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1dfc3-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="1dfc3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1dfc3-107">EXAMPLES</span></span>

## <span data-ttu-id="1dfc3-108">OS</span><span class="sxs-lookup"><span data-stu-id="1dfc3-108">PARAMETERS</span></span>

### <span data-ttu-id="1dfc3-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dfc3-109">-Name</span></span>
<span data-ttu-id="1dfc3-110">Especifica o nome do cofre para consulta.</span><span class="sxs-lookup"><span data-stu-id="1dfc3-110">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="1dfc3-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dfc3-111">-ResourceGroupName</span></span>
<span data-ttu-id="1dfc3-112">Especifica o nome do grupo de recursos do Azure no qual criar ou do qual recuperar o objeto de serviços de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="1dfc3-112">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="1dfc3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dfc3-113">-DefaultProfile</span></span>
<span data-ttu-id="1dfc3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1dfc3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dfc3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dfc3-115">CommonParameters</span></span>
<span data-ttu-id="1dfc3-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dfc3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dfc3-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dfc3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dfc3-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1dfc3-118">INPUTS</span></span>

## <span data-ttu-id="1dfc3-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1dfc3-119">OUTPUTS</span></span>

### <span data-ttu-id="1dfc3-120">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Recoveryservices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="1dfc3-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="1dfc3-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1dfc3-121">NOTES</span></span>

## <span data-ttu-id="1dfc3-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1dfc3-122">RELATED LINKS</span></span>

[<span data-ttu-id="1dfc3-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1dfc3-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="1dfc3-124">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="1dfc3-124">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="1dfc3-125">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="1dfc3-125">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


