---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: 3607835496aa6f99cfd2b42383654180d6b12331
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772988"
---
# <span data-ttu-id="b9f1b-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b9f1b-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="b9f1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9f1b-102">SYNOPSIS</span></span>

<span data-ttu-id="b9f1b-103">Obtém uma lista de cofres de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b9f1b-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="b9f1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9f1b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9f1b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9f1b-105">DESCRIPTION</span></span>

<span data-ttu-id="b9f1b-106">O cmdlet **Get-AzRecoveryServicesVault** Obtém uma lista de cofres de serviços de recuperação na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="b9f1b-106">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="b9f1b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9f1b-107">EXAMPLES</span></span>

### <span data-ttu-id="b9f1b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9f1b-108">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="b9f1b-109">Obter a lista de cofre na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="b9f1b-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="b9f1b-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b9f1b-110">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="b9f1b-111">Obter a lista de cofre no grupo de recursos na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="b9f1b-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="b9f1b-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b9f1b-112">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="b9f1b-113">Obter o cofre no grupo de recursos com o nome fornecido.</span><span class="sxs-lookup"><span data-stu-id="b9f1b-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="b9f1b-114">OS</span><span class="sxs-lookup"><span data-stu-id="b9f1b-114">PARAMETERS</span></span>

### <span data-ttu-id="b9f1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f1b-115">-DefaultProfile</span></span>

<span data-ttu-id="b9f1b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9f1b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9f1b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9f1b-117">-Name</span></span>

<span data-ttu-id="b9f1b-118">Especifica o nome do cofre para consulta.</span><span class="sxs-lookup"><span data-stu-id="b9f1b-118">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="b9f1b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9f1b-119">-ResourceGroupName</span></span>

<span data-ttu-id="b9f1b-120">Especifica o nome do grupo de recursos do Azure do qual recuperar o objeto de serviços de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="b9f1b-120">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="b9f1b-121">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f1b-121">-CommonParameters</span></span>

<span data-ttu-id="b9f1b-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9f1b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f1b-123">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9f1b-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f1b-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9f1b-124">INPUTS</span></span>

### <span data-ttu-id="b9f1b-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b9f1b-125">None</span></span>

## <span data-ttu-id="b9f1b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9f1b-126">OUTPUTS</span></span>

### <span data-ttu-id="b9f1b-127">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="b9f1b-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b9f1b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9f1b-128">NOTES</span></span>

## <span data-ttu-id="b9f1b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9f1b-129">RELATED LINKS</span></span>

[<span data-ttu-id="b9f1b-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b9f1b-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="b9f1b-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b9f1b-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="b9f1b-132">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b9f1b-132">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)