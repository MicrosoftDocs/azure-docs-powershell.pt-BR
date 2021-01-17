---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: f667c0b13de510f7cf3e30e3faca9a93395ac221
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428052"
---
# <span data-ttu-id="a6595-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a6595-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="a6595-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6595-102">SYNOPSIS</span></span>

<span data-ttu-id="a6595-103">Obtém uma lista de cofres de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a6595-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="a6595-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6595-104">SYNTAX</span></span>

### <span data-ttu-id="a6595-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6595-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6595-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6595-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6595-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6595-107">DESCRIPTION</span></span>

<span data-ttu-id="a6595-108">O cmdlet **Get-AzRecoveryServicesVault** Obtém uma lista de cofres de serviços de recuperação na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a6595-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="a6595-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6595-109">EXAMPLES</span></span>

### <span data-ttu-id="a6595-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a6595-110">Example 1</span></span>

```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="a6595-111">Obter a lista de cofre na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="a6595-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="a6595-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a6595-112">Example 2</span></span>

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="a6595-113">Obter a lista de cofre no grupo de recursos na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="a6595-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="a6595-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a6595-114">Example 3</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

<span data-ttu-id="a6595-115">O primeiro cmdlet obtém o cofre no grupo de recursos com o nome fornecido.</span><span class="sxs-lookup"><span data-stu-id="a6595-115">The first cmdlet gets the vault in resource group with given name.</span></span> <span data-ttu-id="a6595-116">Em seguida, acessamos as informações MSI do cofre.</span><span class="sxs-lookup"><span data-stu-id="a6595-116">Then we access the MSI information from the vault.</span></span>

## <span data-ttu-id="a6595-117">OS</span><span class="sxs-lookup"><span data-stu-id="a6595-117">PARAMETERS</span></span>

### <span data-ttu-id="a6595-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6595-118">-DefaultProfile</span></span>

<span data-ttu-id="a6595-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6595-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6595-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6595-120">-Name</span></span>

<span data-ttu-id="a6595-121">Especifica o nome do cofre para consulta.</span><span class="sxs-lookup"><span data-stu-id="a6595-121">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6595-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6595-122">-ResourceGroupName</span></span>

<span data-ttu-id="a6595-123">Especifica o nome do grupo de recursos do Azure do qual recuperar o objeto de serviços de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="a6595-123">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6595-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="a6595-124">-Tag</span></span>

<span data-ttu-id="a6595-125">Especifica as marcas a serem consultadas</span><span class="sxs-lookup"><span data-stu-id="a6595-125">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6595-126">-TagName</span><span class="sxs-lookup"><span data-stu-id="a6595-126">-TagName</span></span>

<span data-ttu-id="a6595-127">Especifica a chave da marcação para consulta</span><span class="sxs-lookup"><span data-stu-id="a6595-127">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6595-128">-TagValue</span><span class="sxs-lookup"><span data-stu-id="a6595-128">-TagValue</span></span>

<span data-ttu-id="a6595-129">Especifica o valor da marcação para consulta</span><span class="sxs-lookup"><span data-stu-id="a6595-129">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6595-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6595-130">CommonParameters</span></span>
<span data-ttu-id="a6595-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6595-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6595-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6595-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6595-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6595-133">INPUTS</span></span>

### <span data-ttu-id="a6595-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a6595-134">None</span></span>

## <span data-ttu-id="a6595-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6595-135">OUTPUTS</span></span>

### <span data-ttu-id="a6595-136">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="a6595-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a6595-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6595-137">NOTES</span></span>
<span data-ttu-id="a6595-138">Get-AzRecoveryServicesVault na versão antiga do AZ. Recoveryservices (<= 2.10.0) não funciona com o AZ. Accounts (>= 1.8.1) devido à referência de assembly incorreta.</span><span class="sxs-lookup"><span data-stu-id="a6595-138">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="a6595-139">O módulo AZ. Recoveryservices precisa ser atualizado para o 2.11.0 ou mais recente se você estiver usando as contas AZ ou AZ mais recentes.</span><span class="sxs-lookup"><span data-stu-id="a6595-139">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="a6595-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6595-140">RELATED LINKS</span></span>

[<span data-ttu-id="a6595-141">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a6595-141">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="a6595-142">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a6595-142">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="a6595-143">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a6595-143">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
