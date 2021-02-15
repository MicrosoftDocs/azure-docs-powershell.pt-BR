---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: f667c0b13de510f7cf3e30e3faca9a93395ac221
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114951"
---
# <span data-ttu-id="12f5b-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="12f5b-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="12f5b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12f5b-102">SYNOPSIS</span></span>

<span data-ttu-id="12f5b-103">Obtém uma lista de cofres dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="12f5b-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="12f5b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12f5b-104">SYNTAX</span></span>

### <span data-ttu-id="12f5b-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="12f5b-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12f5b-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12f5b-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12f5b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="12f5b-107">DESCRIPTION</span></span>

<span data-ttu-id="12f5b-108">O cmdlet **Get-AzRecoveryServicesVault** obtém uma lista de cofres dos Serviços de Recuperação na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="12f5b-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="12f5b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="12f5b-109">EXAMPLES</span></span>

### <span data-ttu-id="12f5b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="12f5b-110">Example 1</span></span>

```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="12f5b-111">Obter a lista do cofre na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="12f5b-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="12f5b-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="12f5b-112">Example 2</span></span>

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="12f5b-113">Obter a lista do cofre no grupo de recursos na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="12f5b-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="12f5b-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="12f5b-114">Example 3</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

<span data-ttu-id="12f5b-115">O primeiro cmdlet obtém o cofre no grupo de recursos com determinado nome.</span><span class="sxs-lookup"><span data-stu-id="12f5b-115">The first cmdlet gets the vault in resource group with given name.</span></span> <span data-ttu-id="12f5b-116">Em seguida, acessamos as informações de MSI do cofre.</span><span class="sxs-lookup"><span data-stu-id="12f5b-116">Then we access the MSI information from the vault.</span></span>

## <span data-ttu-id="12f5b-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12f5b-117">PARAMETERS</span></span>

### <span data-ttu-id="12f5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f5b-118">-DefaultProfile</span></span>

<span data-ttu-id="12f5b-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="12f5b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12f5b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="12f5b-120">-Name</span></span>

<span data-ttu-id="12f5b-121">Especifica o nome do cofre para o que consultar.</span><span class="sxs-lookup"><span data-stu-id="12f5b-121">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="12f5b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12f5b-122">-ResourceGroupName</span></span>

<span data-ttu-id="12f5b-123">Especifica o nome do grupo de recursos do Azure do qual recuperar o objeto especificado dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="12f5b-123">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="12f5b-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="12f5b-124">-Tag</span></span>

<span data-ttu-id="12f5b-125">Especifica as Marcas para consulta</span><span class="sxs-lookup"><span data-stu-id="12f5b-125">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="12f5b-126">-TagName</span><span class="sxs-lookup"><span data-stu-id="12f5b-126">-TagName</span></span>

<span data-ttu-id="12f5b-127">Especifica a chave da marca para consulta</span><span class="sxs-lookup"><span data-stu-id="12f5b-127">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="12f5b-128">-TagValue</span><span class="sxs-lookup"><span data-stu-id="12f5b-128">-TagValue</span></span>

<span data-ttu-id="12f5b-129">Especifica o Valor da Marca para consulta</span><span class="sxs-lookup"><span data-stu-id="12f5b-129">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="12f5b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f5b-130">CommonParameters</span></span>
<span data-ttu-id="12f5b-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12f5b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f5b-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12f5b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f5b-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="12f5b-133">INPUTS</span></span>

### <span data-ttu-id="12f5b-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="12f5b-134">None</span></span>

## <span data-ttu-id="12f5b-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="12f5b-135">OUTPUTS</span></span>

### <span data-ttu-id="12f5b-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="12f5b-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="12f5b-137">Notas</span><span class="sxs-lookup"><span data-stu-id="12f5b-137">NOTES</span></span>
<span data-ttu-id="12f5b-138">Get-AzRecoveryServicesVault em versão antiga do Az.RecoveryServices(<=2.10.0) não pode funcionar com contas do Az.Accounts(>=1,8.1) devido a uma referência de montagem incorreta.</span><span class="sxs-lookup"><span data-stu-id="12f5b-138">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="12f5b-139">O módulo Az.RecoveryServices precisa ser atualizado para 2.11.0 ou mais recente se você estiver usando as contas mais recentes do Az ou do Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="12f5b-139">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="12f5b-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12f5b-140">RELATED LINKS</span></span>

[<span data-ttu-id="12f5b-141">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="12f5b-141">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="12f5b-142">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="12f5b-142">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="12f5b-143">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="12f5b-143">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
