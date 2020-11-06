---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 4c27cc1cadb7d667793aa297303e539bd8db186f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598472"
---
# <span data-ttu-id="c6303-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="c6303-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="c6303-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6303-102">SYNOPSIS</span></span>
<span data-ttu-id="c6303-103">Use somente para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="c6303-103">Use for troubleshooting only.</span></span> <span data-ttu-id="c6303-104">Esse comando irá reverter o certificado do servidor de sincronização de armazenamento usado para descrever a identidade do servidor para o serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c6303-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="c6303-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6303-105">SYNTAX</span></span>

### <span data-ttu-id="c6303-106">Objectparameterset (padrão)</span><span class="sxs-lookup"><span data-stu-id="c6303-106">ObjectParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6303-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6303-107">StringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6303-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6303-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6303-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6303-109">DESCRIPTION</span></span>
<span data-ttu-id="c6303-110">Esse comando irá rolar o certificado do servidor de sincronização de armazenamento usado para descrever a identidade do servidor para o serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c6303-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="c6303-111">Isso deve ser usado em cenários de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="c6303-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="c6303-112">Ao chamar esse comando, o certificado do servidor é substituído, atualizando o serviço de sincronização de armazenamento com o qual esse servidor está registrado também, enviando a parte pública da chave.</span><span class="sxs-lookup"><span data-stu-id="c6303-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="c6303-113">Como um novo certificado é gerado, o tempo de expiração dessa CERT também é atualizado.</span><span class="sxs-lookup"><span data-stu-id="c6303-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="c6303-114">Esse comando também pode ser usado para atualizar um certificado expirado.</span><span class="sxs-lookup"><span data-stu-id="c6303-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="c6303-115">Isso pode acontecer se um servidor estiver offline por um período de tempo prolongado.</span><span class="sxs-lookup"><span data-stu-id="c6303-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="c6303-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6303-116">EXAMPLES</span></span>

### <span data-ttu-id="c6303-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6303-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="c6303-118">Esse comando irá reverter o certificado do servidor local e informar o serviço de sincronização de armazenamento correspondente da nova identidade do servidor, de maneira segura.</span><span class="sxs-lookup"><span data-stu-id="c6303-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="c6303-119">OS</span><span class="sxs-lookup"><span data-stu-id="c6303-119">PARAMETERS</span></span>

### <span data-ttu-id="c6303-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6303-120">-DefaultProfile</span></span>
<span data-ttu-id="c6303-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6303-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6303-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c6303-122">-ParentObject</span></span>
<span data-ttu-id="c6303-123">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c6303-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6303-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c6303-124">-ParentResourceId</span></span>
<span data-ttu-id="c6303-125">ID do recurso pai StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c6303-125">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6303-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6303-126">-PassThru</span></span>
<span data-ttu-id="c6303-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="c6303-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6303-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6303-128">-ResourceGroupName</span></span>
<span data-ttu-id="c6303-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c6303-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6303-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c6303-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="c6303-131">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="c6303-131">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6303-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c6303-132">-Confirm</span></span>
<span data-ttu-id="c6303-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6303-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6303-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6303-134">-WhatIf</span></span>
<span data-ttu-id="c6303-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c6303-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6303-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c6303-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6303-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6303-137">CommonParameters</span></span>
<span data-ttu-id="c6303-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6303-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6303-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6303-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6303-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6303-140">INPUTS</span></span>

### <span data-ttu-id="c6303-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c6303-141">System.String</span></span>

### <span data-ttu-id="c6303-142">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c6303-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="c6303-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6303-143">OUTPUTS</span></span>

### <span data-ttu-id="c6303-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="c6303-144">System.Object</span></span>
## <span data-ttu-id="c6303-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6303-145">NOTES</span></span>

## <span data-ttu-id="c6303-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6303-146">RELATED LINKS</span></span>
