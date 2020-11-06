---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bbc059751ee4713b59f6b915efe32bdf57419be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432926"
---
# <span data-ttu-id="884a1-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="884a1-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="884a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="884a1-102">SYNOPSIS</span></span>
<span data-ttu-id="884a1-103">Obtém uma lista de cofres de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="884a1-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="884a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="884a1-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="884a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="884a1-105">DESCRIPTION</span></span>
<span data-ttu-id="884a1-106">O cmdlet **Get-AzureRmRecoveryServicesVault** Obtém uma lista de cofres de serviços de recuperação na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="884a1-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="884a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="884a1-107">EXAMPLES</span></span>

### <span data-ttu-id="884a1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="884a1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

<span data-ttu-id="884a1-109">Obter a lista de cofre na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="884a1-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="884a1-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="884a1-110">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="884a1-111">Obter a lista de cofre no grupo de recursos na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="884a1-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="884a1-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="884a1-112">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="884a1-113">Obter o cofre no grupo de recursos com o nome fornecido.</span><span class="sxs-lookup"><span data-stu-id="884a1-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="884a1-114">OS</span><span class="sxs-lookup"><span data-stu-id="884a1-114">PARAMETERS</span></span>

### <span data-ttu-id="884a1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="884a1-115">-Name</span></span>
<span data-ttu-id="884a1-116">Especifica o nome do cofre para consulta.</span><span class="sxs-lookup"><span data-stu-id="884a1-116">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="884a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="884a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="884a1-118">Especifica o nome do grupo de recursos do Azure no qual criar ou do qual recuperar o objeto de serviços de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="884a1-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="884a1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="884a1-119">-DefaultProfile</span></span>
<span data-ttu-id="884a1-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="884a1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="884a1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="884a1-121">CommonParameters</span></span>
<span data-ttu-id="884a1-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="884a1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="884a1-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="884a1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="884a1-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="884a1-124">INPUTS</span></span>

### <span data-ttu-id="884a1-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="884a1-125">None</span></span>
<span data-ttu-id="884a1-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="884a1-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="884a1-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="884a1-127">OUTPUTS</span></span>

### <span data-ttu-id="884a1-128">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Recoveryservices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="884a1-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="884a1-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="884a1-129">NOTES</span></span>

## <span data-ttu-id="884a1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="884a1-130">RELATED LINKS</span></span>

[<span data-ttu-id="884a1-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="884a1-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="884a1-132">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="884a1-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="884a1-133">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="884a1-133">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


