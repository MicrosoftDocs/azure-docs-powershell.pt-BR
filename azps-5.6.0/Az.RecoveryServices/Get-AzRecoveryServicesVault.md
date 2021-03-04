---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: a6aa52408cf1befd1c1208258c184be327ff2a15
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887871"
---
# <span data-ttu-id="ddd61-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ddd61-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="ddd61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddd61-102">SYNOPSIS</span></span>

<span data-ttu-id="ddd61-103">Obtém uma lista de cofres dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="ddd61-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="ddd61-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ddd61-104">SYNTAX</span></span>

### <span data-ttu-id="ddd61-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd61-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddd61-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd61-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddd61-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddd61-107">DESCRIPTION</span></span>

<span data-ttu-id="ddd61-108">O cmdlet **Get-AzRecoveryServicesVault** obtém uma lista de cofres dos Serviços de Recuperação na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ddd61-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="ddd61-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddd61-109">EXAMPLES</span></span>

### <span data-ttu-id="ddd61-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ddd61-110">Example 1</span></span>

```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="ddd61-111">Obter a lista de cofres na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="ddd61-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="ddd61-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ddd61-112">Example 2</span></span>

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="ddd61-113">Obter a lista de cofre no grupo de recursos na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="ddd61-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="ddd61-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ddd61-114">Example 3</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

<span data-ttu-id="ddd61-115">O primeiro cmdlet obtém o cofre no grupo de recursos com o nome determinado.</span><span class="sxs-lookup"><span data-stu-id="ddd61-115">The first cmdlet gets the vault in resource group with given name.</span></span> <span data-ttu-id="ddd61-116">Em seguida, acessamos as informações MSI do cofre.</span><span class="sxs-lookup"><span data-stu-id="ddd61-116">Then we access the MSI information from the vault.</span></span>

## <span data-ttu-id="ddd61-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ddd61-117">PARAMETERS</span></span>

### <span data-ttu-id="ddd61-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd61-118">-DefaultProfile</span></span>

<span data-ttu-id="ddd61-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ddd61-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddd61-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ddd61-120">-Name</span></span>

<span data-ttu-id="ddd61-121">Especifica o nome do cofre para o que consultar.</span><span class="sxs-lookup"><span data-stu-id="ddd61-121">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="ddd61-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd61-122">-ResourceGroupName</span></span>

<span data-ttu-id="ddd61-123">Especifica o nome do grupo de recursos do Azure do qual recuperar o objeto Recovery Services especificado.</span><span class="sxs-lookup"><span data-stu-id="ddd61-123">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="ddd61-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="ddd61-124">-Tag</span></span>

<span data-ttu-id="ddd61-125">Especifica as Marcas para as que consultar</span><span class="sxs-lookup"><span data-stu-id="ddd61-125">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="ddd61-126">-TagName</span><span class="sxs-lookup"><span data-stu-id="ddd61-126">-TagName</span></span>

<span data-ttu-id="ddd61-127">Especifica a chave da marca para a consulta</span><span class="sxs-lookup"><span data-stu-id="ddd61-127">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="ddd61-128">-TagValue</span><span class="sxs-lookup"><span data-stu-id="ddd61-128">-TagValue</span></span>

<span data-ttu-id="ddd61-129">Especifica o valor da marca para a consulta</span><span class="sxs-lookup"><span data-stu-id="ddd61-129">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="ddd61-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd61-130">CommonParameters</span></span>
<span data-ttu-id="ddd61-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd61-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd61-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddd61-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd61-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddd61-133">INPUTS</span></span>

### <span data-ttu-id="ddd61-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ddd61-134">None</span></span>

## <span data-ttu-id="ddd61-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ddd61-135">OUTPUTS</span></span>

### <span data-ttu-id="ddd61-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="ddd61-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ddd61-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="ddd61-137">NOTES</span></span>
<span data-ttu-id="ddd61-138">Get-AzRecoveryServicesVault na versão antiga do Az.RecoveryServices(<=2.10.0) não pode funcionar com o Az.Accounts(>=1,8.1) devido à referência incorreta do assembly.</span><span class="sxs-lookup"><span data-stu-id="ddd61-138">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="ddd61-139">O módulo Az.RecoveryServices precisa ser atualizado para 2.11.0 ou mais recente se você estiver usando o Az ou Az.Accounts mais recente.</span><span class="sxs-lookup"><span data-stu-id="ddd61-139">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="ddd61-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddd61-140">RELATED LINKS</span></span>

[<span data-ttu-id="ddd61-141">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ddd61-141">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="ddd61-142">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ddd61-142">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="ddd61-143">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ddd61-143">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
