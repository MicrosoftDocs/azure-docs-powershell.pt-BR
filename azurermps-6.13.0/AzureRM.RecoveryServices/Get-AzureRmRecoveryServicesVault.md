---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 0812fc8aa5673f6475fb822137cffff025003d32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610858"
---
# <span data-ttu-id="ee853-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ee853-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="ee853-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee853-102">SYNOPSIS</span></span>
<span data-ttu-id="ee853-103">Obtém uma lista de cofres de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ee853-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee853-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee853-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee853-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee853-105">DESCRIPTION</span></span>
<span data-ttu-id="ee853-106">O cmdlet **Get-AzureRmRecoveryServicesVault** Obtém uma lista de cofres de serviços de recuperação na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ee853-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="ee853-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee853-107">EXAMPLES</span></span>

### <span data-ttu-id="ee853-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ee853-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

<span data-ttu-id="ee853-109">Obter a lista de cofre na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="ee853-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="ee853-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ee853-110">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="ee853-111">Obter a lista de cofre no grupo de recursos na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="ee853-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="ee853-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ee853-112">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="ee853-113">Obter o cofre no grupo de recursos com o nome fornecido.</span><span class="sxs-lookup"><span data-stu-id="ee853-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="ee853-114">OS</span><span class="sxs-lookup"><span data-stu-id="ee853-114">PARAMETERS</span></span>

### <span data-ttu-id="ee853-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee853-115">-Name</span></span>
<span data-ttu-id="ee853-116">Especifica o nome do cofre para consulta.</span><span class="sxs-lookup"><span data-stu-id="ee853-116">Specifies the name of the vault to query for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee853-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee853-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee853-118">Especifica o nome do grupo de recursos do Azure no qual criar ou do qual recuperar o objeto de serviços de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="ee853-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee853-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee853-119">-DefaultProfile</span></span>
<span data-ttu-id="ee853-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee853-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee853-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee853-121">CommonParameters</span></span>
<span data-ttu-id="ee853-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee853-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee853-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee853-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee853-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee853-124">INPUTS</span></span>

### <span data-ttu-id="ee853-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ee853-125">None</span></span>

## <span data-ttu-id="ee853-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee853-126">OUTPUTS</span></span>

### <span data-ttu-id="ee853-127">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="ee853-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ee853-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee853-128">NOTES</span></span>

## <span data-ttu-id="ee853-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee853-129">RELATED LINKS</span></span>

[<span data-ttu-id="ee853-130">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ee853-130">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="ee853-131">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ee853-131">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="ee853-132">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ee853-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


