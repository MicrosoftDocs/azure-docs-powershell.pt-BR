---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: fcedf52f75b73cc35b7f0e4fd0856600bca6fc71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112720"
---
# <span data-ttu-id="8a84a-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8a84a-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="8a84a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a84a-102">SYNOPSIS</span></span>

<span data-ttu-id="8a84a-103">Obtém uma lista de cofres de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8a84a-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="8a84a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a84a-104">SYNTAX</span></span>

### <span data-ttu-id="8a84a-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a84a-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a84a-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a84a-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a84a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a84a-107">DESCRIPTION</span></span>

<span data-ttu-id="8a84a-108">O cmdlet **Get-AzRecoveryServicesVault** Obtém uma lista de cofres de serviços de recuperação na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8a84a-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="8a84a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a84a-109">EXAMPLES</span></span>

### <span data-ttu-id="8a84a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8a84a-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="8a84a-111">Obter a lista de cofre na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="8a84a-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="8a84a-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8a84a-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="8a84a-113">Obter a lista de cofre no grupo de recursos na assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="8a84a-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="8a84a-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8a84a-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="8a84a-115">Obter o cofre no grupo de recursos com o nome fornecido.</span><span class="sxs-lookup"><span data-stu-id="8a84a-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="8a84a-116">OS</span><span class="sxs-lookup"><span data-stu-id="8a84a-116">PARAMETERS</span></span>

### <span data-ttu-id="8a84a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a84a-117">-DefaultProfile</span></span>

<span data-ttu-id="8a84a-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a84a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a84a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a84a-119">-Name</span></span>

<span data-ttu-id="8a84a-120">Especifica o nome do cofre para consulta.</span><span class="sxs-lookup"><span data-stu-id="8a84a-120">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="8a84a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a84a-121">-ResourceGroupName</span></span>

<span data-ttu-id="8a84a-122">Especifica o nome do grupo de recursos do Azure do qual recuperar o objeto de serviços de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="8a84a-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="8a84a-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="8a84a-123">-Tag</span></span>

<span data-ttu-id="8a84a-124">Especifica as marcas a serem consultadas</span><span class="sxs-lookup"><span data-stu-id="8a84a-124">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="8a84a-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="8a84a-125">-TagName</span></span>

<span data-ttu-id="8a84a-126">Especifica a chave da marcação para consulta</span><span class="sxs-lookup"><span data-stu-id="8a84a-126">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="8a84a-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="8a84a-127">-TagValue</span></span>

<span data-ttu-id="8a84a-128">Especifica o valor da marcação para consulta</span><span class="sxs-lookup"><span data-stu-id="8a84a-128">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="8a84a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a84a-129">CommonParameters</span></span>
<span data-ttu-id="8a84a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a84a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a84a-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a84a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a84a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a84a-132">INPUTS</span></span>

### <span data-ttu-id="8a84a-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8a84a-133">None</span></span>

## <span data-ttu-id="8a84a-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a84a-134">OUTPUTS</span></span>

### <span data-ttu-id="8a84a-135">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="8a84a-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="8a84a-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a84a-136">NOTES</span></span>
<span data-ttu-id="8a84a-137">Get-AzRecoveryServicesVault na versão antiga do AZ. Recoveryservices (<= 2.10.0) não funciona com o AZ. Accounts (>= 1.8.1) devido à referência de assembly incorreta.</span><span class="sxs-lookup"><span data-stu-id="8a84a-137">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="8a84a-138">O módulo AZ. Recoveryservices precisa ser atualizado para o 2.11.0 ou mais recente se você estiver usando as contas AZ ou AZ mais recentes.</span><span class="sxs-lookup"><span data-stu-id="8a84a-138">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="8a84a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a84a-139">RELATED LINKS</span></span>

[<span data-ttu-id="8a84a-140">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8a84a-140">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="8a84a-141">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8a84a-141">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="8a84a-142">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8a84a-142">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
