---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b9154b239e8d4ae2857cba18d3f7dcf9510a62b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427240"
---
# <span data-ttu-id="0f4b7-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0f4b7-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="0f4b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f4b7-102">SYNOPSIS</span></span>
<span data-ttu-id="0f4b7-103">Modifica uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f4b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f4b7-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f4b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f4b7-105">DESCRIPTION</span></span>
<span data-ttu-id="0f4b7-106">O cmdlet **set-AzureRmDataLakeStoreAccount** modifica uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="0f4b7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f4b7-107">EXAMPLES</span></span>

### <span data-ttu-id="0f4b7-108">Exemplo 1: adicionar uma marca a uma conta</span><span class="sxs-lookup"><span data-stu-id="0f4b7-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="0f4b7-109">Esse comando adiciona a marca especificada à conta data Lake Store chamada ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="0f4b7-110">OS</span><span class="sxs-lookup"><span data-stu-id="0f4b7-110">PARAMETERS</span></span>

### <span data-ttu-id="0f4b7-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="0f4b7-111">-AllowAzureIpState</span></span>
<span data-ttu-id="0f4b7-112">Opcionalmente, permitir/bloquear IPs de origem do Azure por meio do firewall.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4b7-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="0f4b7-113">-DefaultGroup</span></span>
<span data-ttu-id="0f4b7-114">Especifica a ID de um grupo de diretórios do AzureActive.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="0f4b7-115">Este grupo é o grupo padrão para arquivos e pastas que você criar.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f4b7-116">-DefaultProfile</span></span>
<span data-ttu-id="0f4b7-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0f4b7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f4b7-118">-Firewallstate</span><span class="sxs-lookup"><span data-stu-id="0f4b7-118">-FirewallState</span></span>
<span data-ttu-id="0f4b7-119">Opcionalmente, habilite ou desabilite as regras de firewall existentes.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4b7-120">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="0f4b7-120">-KeyVersion</span></span>
<span data-ttu-id="0f4b7-121">Se o tipo de criptografia for atribuído pelo usuário, o usuário poderá girar a respectiva versão da chave com esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4b7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f4b7-122">-Name</span></span>
<span data-ttu-id="0f4b7-123">Especifica o nome de uma conta do repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-123">Specifies the name of a Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f4b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f4b7-125">Especifica o nome do grupo de recursos que contém a conta do data Lake Store a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4b7-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="0f4b7-126">-Tag</span></span>
<span data-ttu-id="0f4b7-127">Especifica marcas como pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="0f4b7-128">Você pode usar marcas para identificar uma conta do data Lake Store de outros recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4b7-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="0f4b7-129">-Tier</span></span>
<span data-ttu-id="0f4b7-130">A camada de compromisso desejada para esta conta usar.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4b7-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="0f4b7-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="0f4b7-132">Opcionalmente, habilite ou desabilite os provedores de ID confiáveis existentes.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f4b7-133">CommonParameters</span></span>
<span data-ttu-id="0f4b7-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f4b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f4b7-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f4b7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f4b7-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f4b7-136">INPUTS</span></span>

### <span data-ttu-id="0f4b7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0f4b7-137">System.String</span></span>

### <span data-ttu-id="0f4b7-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0f4b7-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0f4b7-139">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. TrustedIdProviderState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0f4b7-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0f4b7-140">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. Firewallstate, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0f4b7-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0f4b7-141">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. Tiertype, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0f4b7-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0f4b7-142">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0f4b7-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="0f4b7-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f4b7-143">OUTPUTS</span></span>

### <span data-ttu-id="0f4b7-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0f4b7-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="0f4b7-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f4b7-145">NOTES</span></span>

## <span data-ttu-id="0f4b7-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f4b7-146">RELATED LINKS</span></span>

[<span data-ttu-id="0f4b7-147">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0f4b7-147">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="0f4b7-148">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0f4b7-148">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="0f4b7-149">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0f4b7-149">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="0f4b7-150">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0f4b7-150">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


